[![](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/banner2-direct.svg)](https://github.com/vshymanskyy/StandWithUkraine/blob/main/docs/README.md)

---

<div align="center">
	<br>
	<br>
	<img width="240" alt="Ink" src="media/logo.png">
	<br>
	<br>
	<br>
</div>

中文 · [English](./readme_en.md)

> 面向 CLI 的 React。使用组件来构建并测试你的命令行输出。

[![Build Status](https://github.com/vadimdemedes/ink/workflows/test/badge.svg)](https://github.com/vadimdemedes/ink/actions)
[![npm](https://img.shields.io/npm/dm/ink?logo=npm)](https://npmjs.com/package/ink)

Ink 为命令行应用提供了与 React 在浏览器中相同的组件化 UI 构建体验。
它使用 [Yoga](https://github.com/facebook/yoga) 在终端中构建 Flexbox 布局，因此大多数类 CSS 属性在 Ink 中同样可用。
如果你已经熟悉 React，那你其实已经会用 Ink 了。

由于 Ink 是一个 React 渲染器，React 的所有特性都可以使用。
React 的使用方式请参考 [React](https://reactjs.org) 官方文档。
本文档仅记录 Ink 自身的方法。

---

<div align="center">
	<p>
		<p>
			<sup>
				<a href="https://opencollective.com/vadimdemedes">我的开源工作由社区支持 ❤️</a>
			</sup>
		</p>
	</p>
</div>

## Install

```sh
npm install ink react
```

> [!NOTE]
> 本 README 记录的是 Ink 即将发布的版本。最新稳定版请查看 [Ink on npm](https://www.npmjs.com/package/ink)。

## Usage

```jsx
import React, {useState, useEffect} from 'react';
import {render, Text} from 'ink';

const Counter = () => {
	const [counter, setCounter] = useState(0);

	useEffect(() => {
		const timer = setInterval(() => {
			setCounter(previousCounter => previousCounter + 1);
		}, 100);

		return () => {
			clearInterval(timer);
		};
	}, []);

	return <Text color="green">{counter} tests passed</Text>;
};

render(<Counter />);
```

<img src="media/demo.svg" width="600">

## Who's Using Ink?

- [Claude Code](https://github.com/anthropics/claude-code) - Anthropic 打造的代理式编码工具。
- [Gemini CLI](https://github.com/google-gemini/gemini-cli) - Google 打造的代理式编码工具。
- [GitHub Copilot CLI](https://github.com/features/copilot/cli) - 只要说出你想让 shell 做什么。
- [Canva CLI](https://www.canva.dev/docs/apps/canva-cli/) - 用于创建和管理 Canva Apps 的 CLI。
- [Cloudflare's Wrangler](https://github.com/cloudflare/wrangler2) - Cloudflare Workers 的 CLI。
- [Linear](https://linear.app) - Linear 为部署、配置和其他日常维护打造的内部 CLI。
- [Gatsby](https://www.gatsbyjs.org) - 面向极速网站的现代 Web 框架。
- [tap](https://node-tap.org) - JavaScript 的 Test Anything Protocol 库。
- [Terraform CDK](https://github.com/hashicorp/terraform-cdk) - HashiCorp Terraform 的云开发工具包（CDK）。
- [Specify CLI](https://specifyapp.com) - 自动化分发设计令牌（design tokens）。
- [Twilio's SIGNAL](https://github.com/twilio-labs/plugin-signal2020) - Twilio SIGNAL 大会 CLI。[博客](https://www.twilio.com/blog/building-conference-cli-in-react)。
- [Typewriter](https://github.com/segmentio/typewriter) - 从任意 JSON Schema 生成强类型 [Segment](https://segment.com) 分析客户端。
- [Prisma](https://www.prisma.io) - 现代应用统一数据层。
- [Blitz](https://blitzjs.com) - 全栈 React 框架。
- [New York Times](https://github.com/nytimes/kyt) - NYT 在其 `kyt`（封装并管理 Web 应用配置的工具包）中使用 Ink。
- [tink](https://github.com/npm/tink) - 新一代运行时和包管理器。
- [Inkle](https://github.com/jrr/inkle) - 一个 Wordle 游戏。
- [loki](https://github.com/oblador/loki) - Storybook 视觉回归测试工具。
- [Bit](https://github.com/teambit/bit) - 构建、分发并协作组件。
- [Remirror](https://github.com/remirror/remirror) - 友好的世界级编辑器工具集。
- [Prime](https://github.com/birkir/prime) - 开源 GraphQL CMS。
- [emoj](https://github.com/sindresorhus/emoj) - 查找相关 emoji。
- [emma](https://github.com/maticzav/emma-cli) - 轻松查找并安装 npm 包。
- [npm-check-extras](https://github.com/akgondber/npm-check-extras) - 检查过期和未使用依赖，并对选中项执行更新/删除。
- [swiff](https://github.com/simple-integrated-marketing/swiff) - 面向 Web 开发者的多环境省时命令行工具。
- [share](https://github.com/marionebl/share-cli) - 快速分享文件。
- [Kubelive](https://github.com/ameerthehacker/kubelive) - Kubernetes CLI，提供集群及资源的实时数据。
- [changelog-view](https://github.com/jdeniau/changelog-view) - 查看更新日志。
- [cfpush](https://github.com/mamachanko/cfpush) - 交互式 Cloud Foundry 教程。
- [startd](https://github.com/mgrip/startd) - 将 React 组件变成 Web 应用。
- [wiki-cli](https://github.com/hexrcs/wiki-cli) - 搜索维基百科并阅读条目摘要。
- [garson](https://github.com/goliney/garson) - 构建交互式、配置驱动的命令行界面。
- [git-contrib-calendar](https://github.com/giannisp/git-contrib-calendar) - 显示任意 Git 仓库的贡献日历。
- [gitgud](https://github.com/GitGud-org/GitGud) - Git 交互式命令行 GUI。
- [Autarky](https://github.com/pranshuchittora/autarky) - 查找并删除旧的 `node_modules` 目录以释放磁盘空间。
- [fast-cli](https://github.com/sindresorhus/fast-cli) - 测试下载与上传速度。
- [tasuku](https://github.com/privatenumber/tasuku) - 极简任务运行器。
- [mnswpr](https://github.com/mordv/mnswpr) - 扫雷游戏。
- [lrn](https://github.com/krychu/lrn) - 重复记忆学习工具。
- [turdle](https://github.com/mynameisankit/turdle) - 一个 Wordle 游戏。
- [Shopify CLI](https://github.com/Shopify/cli) - 为 Shopify 平台构建应用、主题和店面。
- [ToDesktop CLI](https://www.todesktop.com/electron) - 构建 Electron 应用的一体化平台。
- [Walle](https://github.com/Pobepto/walle) - 面向 EVM 网络的全功能加密钱包。
- [Sudoku](https://github.com/mrozio13pl/sudoku-in-terminal) - 数独游戏。
- [Sea Trader](https://github.com/zyishai/sea-trader) - 受 Taipan! 启发的贸易模拟游戏。
- [srtd](https://github.com/t1mmen/srtd) - Supabase 项目的 SQL 模板实时重载工具。
- [tweakcc](https://github.com/Piebald-AI/tweakcc) - 自定义 Claude Code 样式。
- [argonaut](https://github.com/darksworm/argonaut) - 管理 Argo CD 资源。
- [Qodo Command](https://github.com/qodo-ai/command) - 构建、运行和管理 AI 代理。
- [Nanocoder](https://github.com/nano-collective/nanocoder) - 社区构建的本地优先 AI 编码代理，支持多提供方。
- [dev3000](https://github.com/vercel-labs/dev3000) - AI 代理 MCP 编排器与开发者浏览器。
- [Neovate Code](https://github.com/neovateai/neovate-code) - AntGroup 打造的代理式编码工具。
- [instagram-cli](https://github.com/supreme-gg-gg/instagram-cli) - Instagram 客户端。
- [ElevenLabs CLI](https://github.com/elevenlabs/cli) - ElevenLabs agents 客户端。
- [SSH AI Chat](https://github.com/miantiao-me/ssh-ai-chat) - 通过 SSH 与 AI 对话。

_(欢迎 PR。请在末尾追加新条目。仓库需 100+ stars，并且要展示 Ink 超越基础列表选择器的用法。)_

## Contents

- [Getting Started](#getting-started)
- [App Lifecycle](#app-lifecycle)
- [Components](#components)
  - [`<Text>`](#text)
  - [`<Box>`](#box)
  - [`<Newline>`](#newline)
  - [`<Spacer>`](#spacer)
  - [`<Static>`](#static)
  - [`<Transform>`](#transform)
- [Hooks](#hooks)
  - [`useInput`](#useinputinputhandler-options)
  - [`usePaste`](#usepastehandler-options)
  - [`useApp`](#useapp)
  - [`useStdin`](#usestdin)
  - [`useStdout`](#usestdout)
  - [`useBoxMetrics`](#useboxmetricsref)
  - [`useStderr`](#usestderr)
  - [`useWindowSize`](#usewindowsize)
  - [`useFocus`](#usefocusoptions)
  - [`useFocusManager`](#usefocusmanager)
  - [`useCursor`](#usecursor)
- [API](#api)
- [Testing](#testing)
- [Using React Devtools](#using-react-devtools)
- [Screen Reader Support](#screen-reader-support)
- [Useful Components](#useful-components)
- [Useful Hooks](#useful-hooks)
- [Recipes](#recipes)
- [Examples](#examples)
- [Continuous Integration](#continuous-integration)

## Getting Started

使用 [create-ink-app](https://github.com/vadimdemedes/create-ink-app) 可以快速搭建一个基于 Ink 的 CLI。

```sh
npx create-ink-app my-ink-cli
```

或者创建一个 TypeScript 项目：

```sh
npx create-ink-app --typescript my-ink-cli
```

<details><summary>手动 JavaScript 配置</summary>
<p>
Ink 需要与你在浏览器 React 应用中相同的 Babel 配置。

请使用 React preset 配置 Babel，以确保本 README 中的示例都能正常工作。
在 [安装 Babel](https://babeljs.io/docs/en/usage) 后，安装 `@babel/preset-react`，并在 `babel.config.json` 中加入以下配置：

```sh
npm install --save-dev @babel/preset-react
```

```json
{
	"presets": ["@babel/preset-react"]
}
```

接着，创建 `source.js` 文件，在其中编写使用 Ink 的代码：

```jsx
import React from 'react';
import {render, Text} from 'ink';

const Demo = () => <Text>Hello World</Text>;

render(<Demo />);
```

然后用 Babel 转译该文件：

```sh
npx babel source.js -o cli.js
```

现在你可以使用 Node.js 运行 `cli.js`：

```sh
node cli
```

如果你不希望在开发时先转译文件，可以使用 [import-jsx](https://github.com/vadimdemedes/import-jsx) 或 [@esbuild-kit/esm-loader](https://github.com/esbuild-kit/esm-loader) 直接 `import` JSX 文件并按需即时转译。

</p>
</details>

Ink 使用 [Yoga](https://github.com/facebook/yoga) 这个 Flexbox 布局引擎，在 CLI 中构建优秀界面，并沿用你在浏览器开发中熟悉的类 CSS 属性。
要记住的一点是：每个元素都是 Flexbox 容器。
你可以把它理解为浏览器中的每个 `<div>` 都默认带有 `display: flex`。
有关 Flexbox 布局的使用方式，请参考下文内置组件 [`<Box>`](#box) 的说明。
注意，所有文本都必须包裹在 [`<Text>`](#text) 组件中。

## App Lifecycle

Ink 应用本质上是一个 Node.js 进程，因此它只会在事件循环中仍有活动任务（计时器、未完成的 Promise、监听 `stdin` 的 [`useInput`](#useinputinputhandler-options) 等）时保持存活。
如果你的组件树中没有异步任务，应用会渲染一次后立即退出。

要退出应用，可以按 **Ctrl+C**（默认通过 [`exitOnCtrlC`](#exitonctrlc) 启用），在组件内通过 [`useApp`](#useapp) 调用 [`exit()`](#exiterrororresult)，或在 [`render()`](#rendertree-options) 返回对象上调用 [`unmount()`](#unmount)。

使用 [`waitUntilExit()`](#waituntilexit) 可在应用卸载后执行代码：

```jsx
const {waitUntilExit} = render(<MyApp />);

await waitUntilExit();

console.log('App exited');
```

## Components

### `<Text>`

该组件用于显示文本，并支持加粗、下划线、斜体、删除线等样式。

```jsx
import {render, Text} from 'ink';

const Example = () => (
	<>
		<Text color="green">I am green</Text>
		<Text color="black" backgroundColor="white">
			I am black on white
		</Text>
		<Text color="#ffffff">I am white</Text>
		<Text bold>I am bold</Text>
		<Text italic>I am italic</Text>
		<Text underline>I am underline</Text>
		<Text strikethrough>I am strikethrough</Text>
		<Text inverse>I am inversed</Text>
	</>
);

render(<Example />);
```

> [!NOTE]
> `<Text>` 内只允许文本节点以及嵌套的 `<Text>` 组件。例如，不能在 `<Text>` 中使用 `<Box>` 组件。

#### color

Type: `string`

修改文本颜色。
Ink 底层使用 [chalk](https://github.com/chalk/chalk)，因此支持其全部能力。

```jsx
<Text color="green">Green</Text>
<Text color="#005cc5">Blue</Text>
<Text color="rgb(232, 131, 136)">Red</Text>
```

<img src="media/text-color.jpg" width="247">

#### backgroundColor

Type: `string`

与上面的 `color` 相同，但用于背景色。

```jsx
<Text backgroundColor="green" color="white">Green</Text>
<Text backgroundColor="#005cc5" color="white">Blue</Text>
<Text backgroundColor="rgb(232, 131, 136)" color="white">Red</Text>
```

<img src="media/text-backgroundColor.jpg" width="226">

#### dimColor

Type: `boolean` 
Default: `false`

降低颜色亮度（使其更暗）。

```jsx
<Text color="red" dimColor>
	Dimmed Red
</Text>
```

<img src="media/text-dimColor.jpg" width="138">

#### bold

Type: `boolean` 
Default: `false`

将文本设为粗体。

#### italic

Type: `boolean` 
Default: `false`

将文本设为斜体。

#### underline

Type: `boolean` 
Default: `false`

给文本添加下划线。

#### strikethrough

Type: `boolean` 
Default: `false`

给文本添加删除线。

#### inverse

Type: `boolean` 
Default: `false`

反转前景色与背景色。

```jsx
<Text inverse color="yellow">
	Inversed Yellow
</Text>
```

<img src="media/text-inverse.jpg" width="138">

#### wrap

Type: `string` 
Allowed values: `wrap` `truncate` `truncate-start` `truncate-middle` `truncate-end` 
Default: `wrap`

该属性用于在文本宽度大于容器时控制换行或截断行为。
传入 `wrap`（默认值）时，Ink 会对文本进行换行并拆分成多行。
传入 `truncate-*` 时，Ink 会改为截断文本，最终只显示一行，其余内容被截去。

```jsx
<Box width={7}>
	<Text>Hello World</Text>
</Box>
//=> 'Hello nWorld'

// `truncate` is an alias to `truncate-end`
<Box width={7}>
	<Text wrap="truncate">Hello World</Text>
</Box>
//=> 'Hello…'

<Box width={7}>
	<Text wrap="truncate-middle">Hello World</Text>
</Box>
//=> 'He…ld'

<Box width={7}>
	<Text wrap="truncate-start">Hello World</Text>
</Box>
//=> '…World'
```

### `<Box>`

`<Box>` 是用于构建布局的核心 Ink 组件。
它类似浏览器中的 `<div style="display: flex">`。

```jsx
import {render, Box, Text} from 'ink';

const Example = () => (
	<Box margin={2}>
		<Text>This is a box with margin</Text>
	</Box>
);

render(<Example />);
```

#### Dimensions

##### width

Type: `number` `string`

元素宽度（以空格单元为单位）。
你也可以设置为百分比，宽度将基于父元素宽度计算。

```jsx
<Box width={4}>
	<Text>X</Text>
</Box>
//=> 'X   '
```

```jsx
<Box width={10}>
	<Box width="50%">
		<Text>X</Text>
	</Box>
	<Text>Y</Text>
</Box>
//=> 'X    Y'
```

##### height

Type: `number` `string`

元素高度（以行数为单位）。
你也可以设置为百分比，高度将基于父元素高度计算。

```jsx
<Box height={4}>
	<Text>X</Text>
</Box>
//=> 'X n n n'
```

```jsx
<Box height={6} flexDirection="column">
	<Box height="50%">
		<Text>X</Text>
	</Box>
	<Text>Y</Text>
</Box>
//=> 'X n n nY n n'
```

##### minWidth

Type: `number`

设置元素最小宽度。
暂不支持百分比；见 https://github.com/facebook/yoga/issues/872。

##### minHeight

Type: `number` `string`

设置元素最小高度（以行数为单位）。
你也可以设置为百分比，最小高度将基于父元素高度计算。

##### maxWidth

Type: `number`

设置元素最大宽度。
暂不支持百分比；见 https://github.com/facebook/yoga/issues/872。

##### maxHeight

Type: `number` `string`

设置元素最大高度（以行数为单位）。
你也可以设置为百分比，最大高度将基于父元素高度计算。

##### aspectRatio

Type: `number`

定义元素宽高比（width/height）。

请至少与一个尺寸约束（`width`、`height`、`minHeight` 或 `maxHeight`）配合使用，这样 Ink 才能推导出缺失维度。

#### Padding

##### paddingTop

Type: `number` 
Default: `0`

上内边距。

##### paddingBottom

Type: `number` 
Default: `0`

下内边距。

##### paddingLeft

Type: `number` 
Default: `0`

左内边距。

##### paddingRight

Type: `number` 
Default: `0`

右内边距。

##### paddingX

Type: `number` 
Default: `0`

水平内边距。等价于同时设置 `paddingLeft` 和 `paddingRight`。

##### paddingY

Type: `number` 
Default: `0`

垂直内边距。等价于同时设置 `paddingTop` 和 `paddingBottom`。

##### padding

Type: `number` 
Default: `0`

四边内边距。等价于同时设置 `paddingTop`、`paddingBottom`、`paddingLeft` 和 `paddingRight`。

```jsx
<Box paddingTop={2}><Text>Top</Text></Box>
<Box paddingBottom={2}><Text>Bottom</Text></Box>
<Box paddingLeft={2}><Text>Left</Text></Box>
<Box paddingRight={2}><Text>Right</Text></Box>
<Box paddingX={2}><Text>Left and right</Text></Box>
<Box paddingY={2}><Text>Top and bottom</Text></Box>
<Box padding={2}><Text>Top, bottom, left and right</Text></Box>
```

#### Margin

##### marginTop

Type: `number` 
Default: `0`

上外边距。

##### marginBottom

Type: `number` 
Default: `0`

下外边距。

##### marginLeft

Type: `number` 
Default: `0`

左外边距。

##### marginRight

Type: `number` 
Default: `0`

右外边距。

##### marginX

Type: `number` 
Default: `0`

水平外边距。等价于同时设置 `marginLeft` 和 `marginRight`。

##### marginY

Type: `number` 
Default: `0`

垂直外边距。等价于同时设置 `marginTop` 和 `marginBottom`。

##### margin

Type: `number` 
Default: `0`

四边外边距。等价于同时设置 `marginTop`、`marginBottom`、`marginLeft` 和 `marginRight`。

```jsx
<Box marginTop={2}><Text>Top</Text></Box>
<Box marginBottom={2}><Text>Bottom</Text></Box>
<Box marginLeft={2}><Text>Left</Text></Box>
<Box marginRight={2}><Text>Right</Text></Box>
<Box marginX={2}><Text>Left and right</Text></Box>
<Box marginY={2}><Text>Top and bottom</Text></Box>
<Box margin={2}><Text>Top, bottom, left and right</Text></Box>
```

#### Gap

#### gap

Type: `number` 
Default: `0`

元素列与行之间的间距大小。是 `columnGap` 和 `rowGap` 的简写。

```jsx
<Box gap={1} width={3} flexWrap="wrap">
	<Text>A</Text>
	<Text>B</Text>
	<Text>C</Text>
</Box>
// A B
//
// C
```

#### columnGap

Type: `number` 
Default: `0`

元素列之间的间距大小。

```jsx
<Box columnGap={1}>
	<Text>A</Text>
	<Text>B</Text>
</Box>
// A B
```

#### rowGap

Type: `number` 
Default: `0`

元素行之间的间距大小。

```jsx
<Box flexDirection="column" rowGap={1}>
	<Text>A</Text>
	<Text>B</Text>
</Box>
// A
//
// B
```

#### Flex

##### flexGrow

Type: `number` 
Default: `0`

见 [flex-grow](https://css-tricks.com/almanac/properties/f/flex-grow/)。

```jsx
<Box>
	<Text>Label:</Text>
	<Box flexGrow={1}>
		<Text>Fills all remaining space</Text>
	</Box>
</Box>
```

##### flexShrink

Type: `number` 
Default: `1`

见 [flex-shrink](https://css-tricks.com/almanac/properties/f/flex-shrink/)。

```jsx
<Box width={20}>
	<Box flexShrink={2} width={10}>
		<Text>Will be 1/4</Text>
	</Box>
	<Box width={10}>
		<Text>Will be 3/4</Text>
	</Box>
</Box>
```

##### flexBasis

Type: `number` `string`

见 [flex-basis](https://css-tricks.com/almanac/properties/f/flex-basis/)。

```jsx
<Box width={6}>
	<Box flexBasis={3}>
		<Text>X</Text>
	</Box>
	<Text>Y</Text>
</Box>
//=> 'X  Y'
```

```jsx
<Box width={6}>
	<Box flexBasis="50%">
		<Text>X</Text>
	</Box>
	<Text>Y</Text>
</Box>
//=> 'X  Y'
```

##### flexDirection

Type: `string` 
Allowed values: `row` `row-reverse` `column` `column-reverse`

见 [flex-direction](https://css-tricks.com/almanac/properties/f/flex-direction/)。

```jsx
<Box>
	<Box marginRight={1}>
		<Text>X</Text>
	</Box>
	<Text>Y</Text>
</Box>
// X Y

<Box flexDirection="row-reverse">
	<Text>X</Text>
	<Box marginRight={1}>
		<Text>Y</Text>
	</Box>
</Box>
// Y X

<Box flexDirection="column">
	<Text>X</Text>
	<Text>Y</Text>
</Box>
// X
// Y

<Box flexDirection="column-reverse">
	<Text>X</Text>
	<Text>Y</Text>
</Box>
// Y
// X
```

##### flexWrap

Type: `string` 
Allowed values: `nowrap` `wrap` `wrap-reverse`

见 [flex-wrap](https://css-tricks.com/almanac/properties/f/flex-wrap/)。

```jsx
<Box width={2} flexWrap="wrap">
	<Text>A</Text>
	<Text>BC</Text>
</Box>
// A
// B C
```

```jsx
<Box flexDirection="column" height={2} flexWrap="wrap">
	<Text>A</Text>
	<Text>B</Text>
	<Text>C</Text>
</Box>
// A C
// B
```

##### alignItems

Type: `string` 
Allowed values: `flex-start` `center` `flex-end` `stretch` `baseline`

见 [align-items](https://css-tricks.com/almanac/properties/a/align-items/)。

```jsx
<Box alignItems="flex-start">
	<Box marginRight={1}>
		<Text>X</Text>
	</Box>
	<Text>
		A
		<Newline/>
		B
		<Newline/>
		C
	</Text>
</Box>
// X A
//   B
//   C

<Box alignItems="center">
	<Box marginRight={1}>
		<Text>X</Text>
	</Box>
	<Text>
		A
		<Newline/>
		B
		<Newline/>
		C
	</Text>
</Box>
//   A
// X B
//   C

<Box alignItems="flex-end">
	<Box marginRight={1}>
		<Text>X</Text>
	</Box>
	<Text>
		A
		<Newline/>
		B
		<Newline/>
		C
	</Text>
</Box>
//   A
//   B
// X C
```

##### alignSelf

Type: `string` 
Default: `auto` 
Allowed values: `auto` `flex-start` `center` `flex-end` `stretch` `baseline`

见 [align-self](https://css-tricks.com/almanac/properties/a/align-self/)。

```jsx
<Box height={3}>
	<Box alignSelf="flex-start">
		<Text>X</Text>
	</Box>
</Box>
// X
//
//

<Box height={3}>
	<Box alignSelf="center">
		<Text>X</Text>
	</Box>
</Box>
//
// X
//

<Box height={3}>
	<Box alignSelf="flex-end">
		<Text>X</Text>
	</Box>
</Box>
//
//
// X
```

##### alignContent

Type: `string` 
Default: `flex-start` 
Allowed values: `flex-start` `flex-end` `center` `stretch` `space-between` `space-around` `space-evenly`

当 `flexWrap` 产生多行时，定义交叉轴上各 flex 行之间的对齐方式。
见 [align-content](https://css-tricks.com/almanac/properties/a/align-content/)。
与 CSS 默认值（`stretch`）不同，Ink 默认使用 `flex-start`，因此换行后的行会保持紧凑；除非你显式启用拉伸，否则固定高度的 Box 不会出现意外空白行。

##### justifyContent

Type: `string` 
Allowed values: `flex-start` `center` `flex-end` `space-between` `space-around` `space-evenly`

见 [justify-content](https://css-tricks.com/almanac/properties/j/justify-content/)。

```jsx
<Box justifyContent="flex-start">
	<Text>X</Text>
</Box>
// [X      ]

<Box justifyContent="center">
	<Text>X</Text>
</Box>
// [   X   ]

<Box justifyContent="flex-end">
	<Text>X</Text>
</Box>
// [      X]

<Box justifyContent="space-between">
	<Text>X</Text>
	<Text>Y</Text>
</Box>
// [X      Y]

<Box justifyContent="space-around">
	<Text>X</Text>
	<Text>Y</Text>
</Box>
// [  X   Y  ]

<Box justifyContent="space-evenly">
	<Text>X</Text>
	<Text>Y</Text>
</Box>
// [   X   Y   ]
```

#### Position

##### position

Type: `string` 
Allowed values: `relative` `absolute` `static` 
Default: `relative`

控制元素如何定位。

当 `position` 为 `static` 时，`top`、`right`、`bottom` 和 `left` 将被忽略。

##### top

Type: `number` `string`

定位元素的顶部偏移。
也可以设置为父元素尺寸的百分比。

##### right

Type: `number` `string`

定位元素的右侧偏移。
也可以设置为父元素尺寸的百分比。

##### bottom

Type: `number` `string`

定位元素的底部偏移。
也可以设置为父元素尺寸的百分比。

##### left

Type: `number` `string`

定位元素的左侧偏移。
也可以设置为父元素尺寸的百分比。

#### Visibility

##### display

Type: `string` 
Allowed values: `flex` `none` 
Default: `flex`

将该属性设为 `none` 可隐藏元素。

##### overflowX

Type: `string` 
Allowed values: `visible` `hidden` 
Default: `visible`

元素在水平方向上的溢出行为。

##### overflowY

Type: `string` 
Allowed values: `visible` `hidden` 
Default: `visible`

元素在垂直方向上的溢出行为。

##### overflow

Type: `string` 
Allowed values: `visible` `hidden` 
Default: `visible`

同时设置 `overflowX` 与 `overflowY` 的简写。

#### Borders

##### borderStyle

Type: `string` 
Allowed values: `single` `double` `round` `bold` `singleDouble` `doubleSingle` `classic` | `BoxStyle`

以指定样式添加边框。
如果 `borderStyle` 为 `undefined`（默认值），则不会添加边框。
Ink 使用 [`cli-boxes`](https://github.com/sindresorhus/cli-boxes) 模块提供的边框样式。

```jsx
<Box flexDirection="column">
	<Box>
		<Box borderStyle="single" marginRight={2}>
			<Text>single</Text>
		</Box>

		<Box borderStyle="double" marginRight={2}>
			<Text>double</Text>
		</Box>

		<Box borderStyle="round" marginRight={2}>
			<Text>round</Text>
		</Box>

		<Box borderStyle="bold">
			<Text>bold</Text>
		</Box>
	</Box>

	<Box marginTop={1}>
		<Box borderStyle="singleDouble" marginRight={2}>
			<Text>singleDouble</Text>
		</Box>

		<Box borderStyle="doubleSingle" marginRight={2}>
			<Text>doubleSingle</Text>
		</Box>

		<Box borderStyle="classic">
			<Text>classic</Text>
		</Box>
	</Box>
</Box>
```

<img src="media/box-borderStyle.jpg" width="521">

或者，你也可以这样传入自定义边框样式：

```jsx
<Box
	borderStyle={{
		topLeft: '↘',
		top: '↓',
		topRight: '↙',
		left: '→',
		bottomLeft: '↗',
		bottom: '↑',
		bottomRight: '↖',
		right: '←',
	}}
>
	<Text>Custom</Text>
</Box>
```

示例见 [examples/borders](examples/borders/borders.tsx)。

##### borderColor

Type: `string`

修改边框颜色。
是同时设置 `borderTopColor`、`borderRightColor`、`borderBottomColor` 和 `borderLeftColor` 的简写。

```jsx
<Box borderStyle="round" borderColor="green">
	<Text>Green Rounded Box</Text>
</Box>
```

<img src="media/box-borderColor.jpg" width="228">

##### borderTopColor

Type: `string`

修改上边框颜色。
可接受与 `<Text>` 组件中 [`color`](#color) 相同的取值。

```jsx
<Box borderStyle="round" borderTopColor="green">
	<Text>Hello world</Text>
</Box>
```

##### borderRightColor

Type: `string`

修改右边框颜色。
可接受与 `<Text>` 组件中 [`color`](#color) 相同的取值。

```jsx
<Box borderStyle="round" borderRightColor="green">
	<Text>Hello world</Text>
</Box>
```

##### borderBottomColor

Type: `string`

修改下边框颜色。
可接受与 `<Text>` 组件中 [`color`](#color) 相同的取值。

```jsx
<Box borderStyle="round" borderBottomColor="green">
	<Text>Hello world</Text>
</Box>
```

##### borderLeftColor

Type: `string`

修改左边框颜色。
可接受与 `<Text>` 组件中 [`color`](#color) 相同的取值。

```jsx
<Box borderStyle="round" borderLeftColor="green">
	<Text>Hello world</Text>
</Box>
```

##### borderDimColor

Type: `boolean` 
Default: `false`

降低边框颜色亮度。
是同时设置 `borderTopDimColor`、`borderBottomDimColor`、`borderLeftDimColor` 和 `borderRightDimColor` 的简写。

```jsx
<Box borderStyle="round" borderDimColor>
	<Text>Hello world</Text>
</Box>
```

##### borderTopDimColor

Type: `boolean` 
Default: `false`

降低上边框颜色亮度。

```jsx
<Box borderStyle="round" borderTopDimColor>
	<Text>Hello world</Text>
</Box>
```

##### borderBottomDimColor

Type: `boolean` 
Default: `false`

降低下边框颜色亮度。

```jsx
<Box borderStyle="round" borderBottomDimColor>
	<Text>Hello world</Text>
</Box>
```

##### borderLeftDimColor

Type: `boolean` 
Default: `false`

降低左边框颜色亮度。

```jsx
<Box borderStyle="round" borderLeftDimColor>
	<Text>Hello world</Text>
</Box>
```

##### borderRightDimColor

Type: `boolean` 
Default: `false`

降低右边框颜色亮度。

```jsx
<Box borderStyle="round" borderRightDimColor>
	<Text>Hello world</Text>
</Box>
```

##### borderTop

Type: `boolean` 
Default: `true`

决定上边框是否可见。

##### borderRight

Type: `boolean` 
Default: `true`

决定右边框是否可见。

##### borderBottom

Type: `boolean` 
Default: `true`

决定下边框是否可见。

##### borderLeft

Type: `boolean` 
Default: `true`

决定左边框是否可见。

#### Background

##### backgroundColor

Type: `string`

元素背景颜色。

可接受与 `<Text>` 组件中 [`color`](#color) 相同的取值。

```jsx
<Box flexDirection="column">
	<Box backgroundColor="red" width={20} height={5} alignSelf="flex-start">
		<Text>Red background</Text>
	</Box>

	<Box
		backgroundColor="#FF8800"
		width={20}
		height={3}
		marginTop={1}
		alignSelf="flex-start"
	>
		<Text>Orange background</Text>
	</Box>

	<Box
		backgroundColor="rgb(0, 255, 0)"
		width={20}
		height={3}
		marginTop={1}
		alignSelf="flex-start"
	>
		<Text>Green background</Text>
	</Box>
</Box>
```

背景色会填充整个 `<Box>` 区域，并会被子级 `<Text>` 组件继承，除非子组件显式指定自己的 `backgroundColor`。

```jsx
<Box backgroundColor="blue" alignSelf="flex-start">
	<Text>Blue inherited </Text>
	<Text backgroundColor="yellow">Yellow override </Text>
	<Text>Blue inherited again</Text>
</Box>
```

背景色可与边框和内边距协同工作：

```jsx
<Box
	backgroundColor="cyan"
	borderStyle="round"
	padding={1}
	alignSelf="flex-start"
>
	<Text>Background with border and padding</Text>
</Box>
```

示例见 [examples/box-backgrounds](examples/box-backgrounds/box-backgrounds.tsx)。

### `<Newline>`

添加一个或多个换行符（` n`）。
必须在 `<Text>` 组件内部使用。

#### count

Type: `number` 
Default: `1`

插入的换行符数量。

```jsx
import {render, Text, Newline} from 'ink';

const Example = () => (
	<Text>
		<Text color="green">Hello</Text>
		<Newline />
		<Text color="red">World</Text>
	</Text>
);

render(<Example />);
```

输出：

```
Hello
World
```

### `<Spacer>`

一个可伸展的空白区域，会沿其容器布局的主轴方向扩展。
它可作为快捷方式，用于填充元素之间所有可用空间。

例如，在默认主轴方向（`row`）的 `<Box>` 中使用 `<Spacer>`，会将 "Left" 放在左侧，并把 "Right" 推到右侧。

```jsx
import {render, Box, Text, Spacer} from 'ink';

const Example = () => (
	<Box>
		<Text>Left</Text>
		<Spacer />
		<Text>Right</Text>
	</Box>
);

render(<Example />);
```

在垂直主轴（`column`）中，它会将 "Top" 放在容器顶部，并把 "Bottom" 推到底部。
注意容器必须足够高，效果才会明显。

```jsx
import {render, Box, Text, Spacer} from 'ink';

const Example = () => (
	<Box flexDirection="column" height={10}>
		<Text>Top</Text>
		<Spacer />
		<Text>Bottom</Text>
	</Box>
);

render(<Example />);
```

### `<Static>`

`<Static>` 组件会将其输出永久渲染在其他内容之上。
它非常适合用于展示已完成任务或日志这类内容，即渲染后不会再变化的内容（这也是 "Static" 名称的由来）。

在你无法预先知道或控制要渲染项目数量的场景里，推荐使用 `<Static>`。

例如，[Tap](https://github.com/tapjs/node-tap) 使用 `<Static>` 显示已完成测试列表；[Gatsby](https://github.com/gatsbyjs/gatsby) 使用它在显示实时进度条的同时展示已生成页面列表。

```jsx
import React, {useState, useEffect} from 'react';
import {render, Static, Box, Text} from 'ink';

const Example = () => {
	const [tests, setTests] = useState([]);

	useEffect(() => {
		let completedTests = 0;
		let timer;

		const run = () => {
			// Fake 10 completed tests
			if (completedTests++ < 10) {
				setTests(previousTests => [
					...previousTests,
					{
						id: previousTests.length,
						title: `Test #${previousTests.length + 1}`,
					},
				]);

				timer = setTimeout(run, 100);
			}
		};

		run();

		return () => {
			clearTimeout(timer);
		};
	}, []);

	return (
		<>
			{/* This part will be rendered once to the terminal */}
			<Static items={tests}>
				{test => (
					<Box key={test.id}>
						<Text color="green">✔ {test.title}</Text>
					</Box>
				)}
			</Static>

			{/* This part keeps updating as state changes */}
			<Box marginTop={1}>
				<Text dimColor>Completed tests: {tests.length}</Text>
			</Box>
		</>
	);
};

render(<Example />);
```

> [!NOTE]
> `<Static>` 只会渲染 `items` 属性中新增加的项目，并忽略之前已渲染过的项目。这意味着当你向 `items` 数组新增项目时，对旧项目的修改不会触发重新渲染。

`<Static>` 的完整示例见 [examples/static](examples/static/static.tsx)。

#### items

Type: `Array`

一个数组（元素类型不限），通过组件子函数对每个项目进行渲染。

#### style

Type: `object`

应用到子元素容器的样式。
支持的属性见 [`<Box>`](#box)。

```jsx
<Static items={...} style={{padding: 1}}>
	{...}
</Static>
```

#### children(item)

Type: `Function`

用于渲染 `items` 数组中每一项的函数。
第一个参数是当前项本身，第二个参数是该项在 `items` 数组中的索引。

注意：根组件必须分配 `key`。

```jsx
<Static items={['a', 'b', 'c']}>
	{(item, index) => {
		// This function is called for every item in ['a', 'b', 'c']
		// `item` is 'a', 'b', 'c'
		// `index` is 0, 1, 2
		return (
			<Box key={index}>
				<Text>Item: {item}</Text>
			</Box>
		);
	}}
</Static>
```

### `<Transform>`

在 React 组件被写入输出之前，对其字符串表示进行转换。
例如，你可能希望给文本应用[渐变效果](https://github.com/sindresorhus/ink-gradient)、[添加可点击链接](https://github.com/sindresorhus/ink-link)，或[创建文字特效](https://github.com/sindresorhus/ink-big-text)。
这些场景无法直接接收 React 节点作为输入；它们期望的是字符串。
`<Transform>` 组件正是为此而生：它会提供子组件输出的字符串，并允许你按任意方式转换。

> [!NOTE]
> `<Transform>` 只能应用于 `<Text>` 子组件，且不应改变输出的尺寸；否则布局会不正确。

> [!IMPORTANT]
> 当子元素使用 `<Text>` 的样式属性（例如 `color`、`bold`）时，传给 `transform` 的字符串会包含 [ANSI 转义码](https://en.wikipedia.org/wiki/ANSI_escape_code)。如果你的转换会处理空白字符或执行类似 `.trim()` 的字符串操作，可能需要使用 ANSI 感知方法（例如来自 [`slice-ansi`](https://github.com/chalk/slice-ansi) 或 [`strip-ansi`](https://github.com/chalk/strip-ansi)）。

```jsx
import {render, Transform} from 'ink';

const Example = () => (
	<Transform transform={output => output.toUpperCase()}>
		<Text>Hello World</Text>
	</Transform>
);

render(<Example />);
```

由于 `transform` 函数会把所有字符转为大写，最终渲染到终端的输出将是 "HELLO WORLD"，而不是 "Hello World"。

当输出换行成多行时，了解当前正在处理哪一行会很有帮助。

例如，要实现悬挂缩进组件，可以只对首行之外的行添加缩进。

```jsx
import {render, Transform} from 'ink';

const HangingIndent = ({indent = 4, children}) => (
	<Transform
		transform={(line, index) =>
			index === 0 ? line : ' '.repeat(indent) + line
		}
	>
		{children}
	</Transform>
);

const text =
	'WHEN I WROTE the following pages, or rather the bulk of them, ' +
	'I lived alone, in the woods, a mile from any neighbor, in a ' +
	'house which I had built myself, on the shore of Walden Pond, ' +
	'in Concord, Massachusetts, and earned my living by the labor ' +
	'of my hands only. I lived there two years and two months. At ' +
	'present I am a sojourner in civilized life again.';

render(<HangingIndent indent={4}>{text}</HangingIndent>);
```

#### transform(outputLine, index)

Type: `Function`

用于转换子元素输出的函数。
它接收子元素输出并返回转换后的结果。

##### children

Type: `string`

子组件的输出。

##### index

Type: `number`

当前被转换行的零基行号。

## Hooks

### useInput(inputHandler, options?)

一个返回 `void` 的 React Hook，用于处理用户输入。
它比使用 `useStdin` 并监听 `data` 事件更方便。
你传给 `useInput` 的回调会在用户每次输入字符时触发。
不过，如果用户粘贴的是多字符文本，回调只会触发一次，并把整段字符串作为 `input` 传入。
完整示例见 [examples/use-input](examples/use-input/use-input.tsx)。

```jsx
import {useInput} from 'ink';

const UserInput = () => {
	useInput((input, key) => {
		if (input === 'q') {
			// Exit program
		}

		if (key.leftArrow) {
			// Left arrow key pressed
		}
	});

	return …
};
```

#### inputHandler(input, key)

Type: `Function`

你传给 `useInput` 的处理函数会接收两个参数：

##### input

Type: `string`

程序接收到的输入文本。

##### key

Type: `object`

关于被按下按键的便捷信息。

###### key.leftArrow

###### key.rightArrow

###### key.upArrow

###### key.downArrow

Type: `boolean` 
Default: `false`

当按下方向键时，对应属性会为 `true`。
例如，按下左方向键时，`key.leftArrow` 等于 `true`。

###### key.return

Type: `boolean` 
Default: `false`

按下了回车（Enter）键。

###### key.escape

Type: `boolean` 
Default: `false`

按下了 Escape 键。

###### key.ctrl

Type: `boolean` 
Default: `false`

按下了 Ctrl 键。

###### key.shift

Type: `boolean` 
Default: `false`

按下了 Shift 键。

###### key.tab

Type: `boolean` 
Default: `false`

按下了 Tab 键。

###### key.backspace

Type: `boolean` 
Default: `false`

按下了 Backspace 键。

###### key.delete

Type: `boolean` 
Default: `false`

按下了 Delete 键。

###### key.pageDown

###### key.pageUp

Type: `boolean` 
Default: `false`

当按下 Page Up 或 Page Down 键时，对应属性会为 `true`。
例如，按下 Page Down 时，`key.pageDown` 等于 `true`。

###### key.home

###### key.end

Type: `boolean` 
Default: `false`

当按下 Home 或 End 键时，对应属性会为 `true`。
例如，按下 End 时，`key.end` 等于 `true`。

###### key.meta

Type: `boolean` 
Default: `false`

按下了 [Meta 键](https://en.wikipedia.org/wiki/Meta_key)。

###### key.super

Type: `boolean` 
Default: `false`

按下了 Super 键（macOS 上为 Cmd，Windows 上为 Win）。需要启用 [kitty keyboard protocol](#kittykeyboard)。

###### key.hyper

Type: `boolean` 
Default: `false`

按下了 Hyper 键。需要启用 [kitty keyboard protocol](#kittykeyboard)。

###### key.capsLock

Type: `boolean` 
Default: `false`

Caps Lock 处于激活状态。需要启用 [kitty keyboard protocol](#kittykeyboard)。

###### key.numLock

Type: `boolean` 
Default: `false`

Num Lock 处于激活状态。需要启用 [kitty keyboard protocol](#kittykeyboard)。

###### key.eventType

Type: `'press' | 'repeat' | 'release'` 
Default: `undefined`

按键事件类型。仅在启用 [kitty keyboard protocol](#kittykeyboard) 时可用。未启用时该属性为 `undefined`。

#### options

Type: `object`

##### isActive

Type: `boolean` 
Default: `true`

启用或禁用用户输入捕获。
当同时使用多个 `useInput` Hook 时，这可以避免同一输入被重复处理。

### usePaste(handler, options?)

一个 React Hook，会在用户粘贴文本时调用 `handler`。Hook 激活期间会自动开启 Bracketed paste mode（` x1b[?2004h`），因此粘贴内容会以单个字符串送达，而不会被误解为逐个按键事件。

`usePaste` 和 `useInput` 可以在同一个组件中同时使用。它们工作在不同事件通道上，因此当 `usePaste` 激活时，粘贴内容不会转发给 `useInput` 处理器。

```jsx
import {useInput, usePaste} from 'ink';

const MyInput = () => {
	useInput((input, key) => {
		// Only receives typed characters and key events, not pasted text.
		if (key.return) {
			// Submit
		}
	});

	usePaste((text) => {
		// Receives the full pasted string, including newlines.
		console.log('Pasted:', text);
	});

	return …
};
```

#### handler(text)

Type: `Function`

每当用户粘贴文本时，会以完整字符串调用该函数。该字符串会按原样传递，换行、转义序列及其他特殊字符都会被完整保留。

##### text

Type: `string`

粘贴的文本。

#### options

Type: `object`

##### isActive

Type: `boolean` 
Default: `true`

启用或禁用粘贴处理器。当多个组件使用 `usePaste` 且一次只应激活一个时，这很有用。

### useApp()

一个返回应用生命周期方法的 React Hook。

#### exit(errorOrResult?)

Type: `Function`

退出（卸载）整个 Ink 应用。

##### errorOrResult

Type: `Error | unknown`

可选值，用于控制 [`waitUntilExit`](#waituntilexit) 的完成方式：

- `exit()` 以 `undefined` resolve。
- `exit(error)` 当 `error` 是 `Error` 时 reject。
- `exit(value)` 以 `value` resolve。

```js
import {useEffect} from 'react';
import {useApp} from 'ink';

const Example = () => {
	const {exit} = useApp();

	// Exit the app after 5 seconds
	useEffect(() => {
		setTimeout(() => {
			exit();
		}, 5000);
	}, [exit]);

	return …
};
```

#### waitUntilRenderFlush()

Type: `Function`

返回一个 Promise，在待处理渲染输出被刷新到 stdout 后完成。

```js
import {useEffect} from 'react';
import {useApp} from 'ink';

const Example = () => {
	const {waitUntilRenderFlush} = useApp();

	useEffect(() => {
		void (async () => {
			await waitUntilRenderFlush();
			runNextCommand();
		})();
	}, [waitUntilRenderFlush]);

	return …;
};
```

### useStdin()

一个 React Hook，返回 stdin 流以及与 stdin 相关的工具方法。

#### stdin

Type: `stream.Readable` 
Default: `process.stdin`

传给 `render()` 的 `options.stdin`，或默认的 `process.stdin`。
当你的应用需要处理用户输入时很有用。

```js
import {useStdin} from 'ink';

const Example = () => {
	const {stdin} = useStdin();

	return …
};
```

#### isRawModeSupported

Type: `boolean`

一个布尔标记，用于判断当前 `stdin` 是否支持 `setRawMode`。
使用 `setRawMode` 的组件可以借助 `isRawModeSupported` 在不支持 raw mode 的环境中优雅降级。

```jsx
import {useStdin} from 'ink';

const Example = () => {
	const {isRawModeSupported} = useStdin();

	return isRawModeSupported ? (
		<MyInputComponent />
	) : (
		<MyComponentThatDoesntUseInput />
	);
};
```

#### setRawMode(isRawModeEnabled)

Type: `function`

##### isRawModeEnabled

Type: `boolean`

参见 [`setRawMode`](https://nodejs.org/api/tty.html#tty_readstream_setrawmode_mode)。
Ink 暴露这个函数是为了正确处理 <kbd>Ctrl</kbd>+<kbd>C</kbd>，因此你应使用 Ink 提供的 `setRawMode`，而不是 `process.stdin.setRawMode`。

**Warning:** 除非当前 `stdin` 支持 `setRawMode`，否则此函数会抛出异常。请使用 [`isRawModeSupported`](#israwmodesupported) 先行检测。

```js
import {useStdin} from 'ink';

const Example = () => {
	const {setRawMode} = useStdin();

	useEffect(() => {
		setRawMode(true);

		return () => {
			setRawMode(false);
		};
	});

	return …
};
```

### useStdout()

一个 React Hook，返回 Ink 渲染输出所使用的 stdout 流以及相关工具方法。

#### stdout

Type: `stream.Writable` 
Default: `process.stdout`

```js
import {useStdout} from 'ink';

const Example = () => {
	const {stdout} = useStdout();

	return …
};
```

#### write(data)

在保持 Ink 输出正常显示的同时，向 stdout 写入任意字符串。
当你希望在 Ink 渲染之外显示外部信息，并确保两者不冲突时非常有用。
它与 `<Static>` 类似，但不能接收组件，只能处理字符串。

##### data

Type: `string`

要写入 stdout 的数据。

```js
import {useStdout} from 'ink';

const Example = () => {
	const {write} = useStdout();

	useEffect(() => {
		// Write a single message to stdout, above Ink's output
		write('Hello from Ink to stdout n');
	}, []);

	return …
};
```

更多用法示例见 [examples/use-stdout](examples/use-stdout/use-stdout.tsx)。

### useBoxMetrics(ref)

一个 React Hook，返回被跟踪 Box 元素的当前布局度量信息。
当布局变化时（例如终端尺寸变化、兄弟节点或内容变化、位置变化），它会自动更新。

可使用 `hasMeasured` 判断当前跟踪元素是否已完成测量。

#### ref

Type: `React.RefObject<DOMElement>`

指向要跟踪的 `<Box>` 元素的 ref。

```jsx
import {useRef} from 'react';
import {Box, Text, useBoxMetrics} from 'ink';

const Example = () => {
	const ref = useRef(null);
	const {width, height, left, top, hasMeasured} = useBoxMetrics(ref);

	return (
		<Box ref={ref}>
			<Text>
				{hasMeasured ? `${width}x${height} at ${left},${top}` : 'Measuring...'}
			</Text>
		</Box>
	);
};
```

#### width

Type: `number`

元素宽度。

#### height

Type: `number`

元素高度。

#### left

Type: `number`

到父元素左边缘的距离。

#### top

Type: `number`

到父元素上边缘的距离。

#### hasMeasured

Type: `boolean`

当前跟踪元素是否已完成测量。

> [!NOTE]
> 在首次布局完成前，该 Hook 返回 `{width: 0, height: 0, left: 0, top: 0}`。当跟踪 ref 脱离挂载时，也会返回全零。

### useStderr()

一个 React Hook，返回 stderr 流以及与 stderr 相关的工具方法。

#### stderr

Type: `stream.Writable` 
Default: `process.stderr`

stderr 流。

```js
import {useStderr} from 'ink';

const Example = () => {
	const {stderr} = useStderr();

	return …
};
```

#### write(data)

在保持 Ink 输出正常显示的同时，向 stderr 写入任意字符串。

当你希望在 Ink 渲染之外显示外部信息，并确保两者不冲突时非常有用。
它与 `<Static>` 类似，但不能接收组件，只能处理字符串。

##### data

Type: `string`

要写入 stderr 的数据。

```js
import {useStderr} from 'ink';

const Example = () => {
	const {write} = useStderr();

	useEffect(() => {
		// Write a single message to stderr, above Ink's output
		write('Hello from Ink to stderr n');
	}, []);

	return …
};
```

### useWindowSize()

一个 React Hook，返回当前终端尺寸，并在终端大小变化时重新渲染组件。

```js
import {Text, useWindowSize} from 'ink';

const Example = () => {
	const {columns, rows} = useWindowSize();

	return (
		<Text>
			{columns}x{rows}
		</Text>
	);
};
```

#### columns

Type: `number`

列数（水平字符单元数）。

#### rows

Type: `number`

行数（垂直字符单元数）。

> [!NOTE]
> 当终端变窄时，可能会短暂出现残影行，具体取决于终端模拟器的重排行为。

### useFocus(options?)

一个 React Hook，返回当前组件的焦点状态和焦点控制能力。
使用 `useFocus` Hook 的组件会变为 Ink 中“可聚焦”的组件，因此当用户按下 <kbd>Tab</kbd> 时，Ink 会将焦点切换到该组件。
如果有多个组件调用了 `useFocus` Hook，焦点会按这些组件的渲染顺序依次分配。
该 Hook 返回一个包含 `isFocused` 布尔属性的对象，用于判断当前组件是否获得焦点。

#### options

##### autoFocus

Type: `boolean` 
Default: `false`

如果当前没有活动（已聚焦）组件，则自动将焦点给该组件。

##### isActive

Type: `boolean` 
Default: `true`

启用或禁用该组件的焦点能力，同时保持其在可聚焦组件列表中的位置。
这对于暂时禁用的输入组件很有用。

##### id

Type: `string` 
Required: `false`

为组件设置焦点 ID，可用于以编程方式聚焦该组件。这对包含大量可聚焦元素的大型界面很有用，避免必须逐个循环切换。

```jsx
import {render, useFocus, Text} from 'ink';

const Example = () => {
	const {isFocused} = useFocus();

	return <Text>{isFocused ? 'I am focused' : 'I am not focused'}</Text>;
};

render(<Example />);
```

示例见 [examples/use-focus](examples/use-focus/use-focus.tsx) 与 [examples/use-focus-with-id](examples/use-focus-with-id/use-focus-with-id.tsx)。

### useFocusManager()

一个 React Hook，返回用于管理可聚焦组件焦点的方法。

#### enableFocus()

为所有组件启用焦点管理。

> [!NOTE]
> 除非你曾禁用焦点管理，否则通常无需手动调用此方法。焦点管理默认已启用。

```js
import {useFocusManager} from 'ink';

const Example = () => {
	const {enableFocus} = useFocusManager();

	useEffect(() => {
		enableFocus();
	}, []);

	return …
};
```

#### disableFocus()

禁用所有组件的焦点管理。
当前活动组件（若存在）将失去焦点。

```js
import {useFocusManager} from 'ink';

const Example = () => {
	const {disableFocus} = useFocusManager();

	useEffect(() => {
		disableFocus();
	}, []);

	return …
};
```

#### focusNext()

将焦点切换到下一个可聚焦组件。
如果当前没有活动组件，则会聚焦第一个可聚焦组件。
如果当前活动组件已是列表最后一个，则会回到第一个可聚焦组件。

> [!NOTE]
> 用户按下 <kbd>Tab</kbd> 时，Ink 会调用该方法。

```js
import {useFocusManager} from 'ink';

const Example = () => {
	const {focusNext} = useFocusManager();

	useEffect(() => {
		focusNext();
	}, []);

	return …
};
```

#### focusPrevious()

将焦点切换到上一个可聚焦组件。
如果当前没有活动组件，则会聚焦第一个可聚焦组件。
如果当前活动组件已是列表第一个，则会切换到最后一个可聚焦组件。

> [!NOTE]
> 用户按下 <kbd>Shift</kbd>+<kbd>Tab</kbd> 时，Ink 会调用该方法。

```js
import {useFocusManager} from 'ink';

const Example = () => {
	const {focusPrevious} = useFocusManager();

	useEffect(() => {
		focusPrevious();
	}, []);

	return …
};
```

#### focus(id)

##### id

Type: `string`

将焦点切换到指定 [`id`](#id) 的组件。
若不存在该 ID 对应组件，焦点不会改变。

```js
import {useFocusManager, useInput} from 'ink';

const Example = () => {
	const {focus} = useFocusManager();

	useInput(input => {
		if (input === 's') {
			// Focus the component with focus ID 'someId'
			focus('someId');
		}
	});

	return …
};
```

#### activeId

Type: `string | undefined`

当前聚焦组件的 ID；若无组件聚焦，则为 `undefined`。

```js
import {Text, useFocusManager} from 'ink';

const Example = () => {
	const {activeId} = useFocusManager();

	return <Text>Focused: {activeId ?? 'none'}</Text>;
};
```

### useCursor()

一个 React Hook，返回在每次渲染后控制终端光标位置的方法。
这对 IME（输入法编辑器）支持至关重要，因为正在组合的字符需要显示在光标位置。

```jsx
import {useState} from 'react';
import {Box, Text, useCursor} from 'ink';
import stringWidth from 'string-width';

const TextInput = () => {
	const [text, setText] = useState('');
	const {setCursorPosition} = useCursor();

	const prompt = '> ';
	setCursorPosition({x: stringWidth(prompt + text), y: 1});

	return (
		<Box flexDirection="column">
			<Text>Type here:</Text>
			<Text>
				{prompt}
				{text}
			</Text>
		</Box>
	);
};
```

#### setCursorPosition(position)

设置相对于 Ink 输出的光标位置。传入 `undefined` 可隐藏光标。

##### position

Type: `object | undefined`

对于包含宽字符（CJK、emoji）的字符串，请使用 [`string-width`](https://github.com/sindresorhus/string-width) 计算 `x`。

完整示例见 [examples/cursor-ime](examples/cursor-ime/cursor-ime.tsx)。

###### x

Type: `number`

列位置（从 0 开始）。

###### y

Type: `number`

相对于 Ink 输出顶部的行位置（0 = 第一行）。

### useIsScreenReaderEnabled()

一个 React Hook，返回当前是否启用了屏幕阅读器。
当你希望为屏幕阅读器渲染不同输出时很有用。

```jsx
import {useIsScreenReaderEnabled, Text} from 'ink';

const Example = () => {
	const isScreenReaderEnabled = useIsScreenReaderEnabled();

	return (
		<Text>
			{isScreenReaderEnabled
				? 'Screen reader is enabled'
				: 'Screen reader is disabled'}
		</Text>
	);
};
```

## API

#### render(tree, options?)

Returns: [`Instance`](#instance)

挂载组件并渲染输出。

##### tree

Type: `ReactNode`

##### options

Type: `object`

###### stdout

Type: `stream.Writable` 
Default: `process.stdout`

应用渲染到的输出流。

###### stdin

Type: `stream.Readable` 
Default: `process.stdin`

应用监听输入的输入流。

###### stderr

Type: `stream.Writable` 
Default: `process.stderr`

错误流。

###### exitOnCtrlC

Type: `boolean` 
Default: `true`

配置 Ink 是否监听 Ctrl+C 键盘输入并退出应用。
在 `process.stdin` 处于 [raw mode](https://nodejs.org/api/tty.html#tty_readstream_setrawmode_mode) 时，这一点很重要，因为此时 Ctrl+C 默认会被忽略，进程需自行处理。

###### patchConsole

Type: `boolean` 
Default: `true`

补丁（patch）console 方法，确保 console 输出不会与 Ink 输出混杂。
当调用 `console.*` 方法（如 `console.log()`）时，Ink 会拦截其输出，清除主输出，渲染 console 输出，再重新渲染主输出。
这样两者都可见且互不覆盖。

一旦开始 unmount，Ink 会在 React 清理执行前恢复原生 console。此后卸载阶段的 `console.*` 输出会走正常 console 行为，而不会再被 Ink 重定向。

该功能由 [patch-console](https://github.com/vadimdemedes/patch-console) 提供支持。因此，如果你希望禁用 Ink 的输出拦截并实现自定义方案，也可以直接使用该库。

###### onRender

Type: `({renderTime: number}) => void` 
Default: `undefined`

在每次渲染和重渲染后执行回调，并提供渲染指标。
该回调在 Ink 提交一帧后执行，但不会等待 `stdout`/`stderr` 流回调完成。
若要在输出真正 flush 后执行代码，请使用 [`waitUntilRenderFlush()`](#waituntilrenderflush)。

###### isScreenReaderEnabled

Type: `boolean` 
Default: `process.env['INK_SCREEN_READER'] === 'true'`

启用屏幕阅读器支持。见 [Screen Reader Support](#screen-reader-support)。

###### debug

Type: `boolean` 
Default: `false`

若为 `true`，每次更新都会作为独立输出渲染，而不会替换上一帧。

###### maxFps

Type: `number` 
Default: `30`

渲染更新的最大帧率（FPS）。
用于控制 UI 的更新频率，防止过于频繁重渲染。
更高值意味着更频繁更新，但可能影响性能。
对于高频更新组件，适当降低此值可减少 CPU 占用。

###### incrementalRendering

Type: `boolean` 
Default: `false`

启用增量渲染模式，仅更新变化的行，而不是重绘全部输出。
这可减少闪烁，并提升高频更新 UI 的性能。

###### concurrent

Type: `boolean` 
Default: `false`

启用 React 并发渲染模式。

启用后：

- Suspense 边界能正确处理异步数据获取
- `useTransition` 和 `useDeferredValue` Hook 完全可用
- 更新可被更高优先级任务中断

```jsx
render(<MyApp />, {concurrent: true});
```

> [!NOTE]
> 并发模式会改变渲染时机。部分测试可能需要使用 `act()` 才能正确等待更新。未卸载时在同一个 stdout 上重复调用 `render()` 不受支持。若需切换渲染模式或创建新实例，请先调用 `unmount()`。

###### interactive

Type: `boolean` 
Default: `true`（在 CI 环境中（通过 [`is-in-ci`](https://github.com/sindresorhus/is-in-ci) 检测）或当 `stdout.isTTY` 为 falsy 时为 `false`）

覆盖自动交互模式检测。

默认情况下，Ink 会基于 CI 检测和 `stdout.isTTY` 判断环境是否交互式。非交互式时，Ink 会跳过终端特有功能，例如 ANSI 擦除序列、光标控制、同步输出、窗口大小监听和 kitty keyboard 自动检测。非静态输出只会在卸载时写出最终帧。

多数用户无需设置此选项。仅当你有一套与内置逻辑不同的交互判断策略时再使用。

> [!NOTE]
> 未卸载时在同一个 stdout 上重复调用 `render()` 不受支持。若需修改该选项或创建新实例，请先调用 `unmount()`。

```jsx
// Use your own detection logic
const isInteractive = myCustomDetection();
render(<MyApp />, {interactive: isInteractive});
```

###### alternateScreen

Type: `boolean` 
Default: `false`

在终端的备用屏幕缓冲区渲染应用。启用后，应用会在独立屏幕中渲染，退出时恢复原有终端内容。这与 vim、htop、less 等程序使用的是同一机制。

注意：处于备用屏幕时，终端滚动回溯缓冲不可用。这是标准终端行为；像 vim 这类程序正是为了避免污染用户滚动历史才使用备用屏幕。

Ink 有意将备用屏幕卸载阶段输出视为可丢弃内容。恢复主屏幕后，它不会保留或重放卸载阶段帧、hook 写入或 `console.*` 输出。

仅在交互模式下有效。若 `interactive` 为 `false` 或处于非交互环境（CI、stdout 被管道重定向），该选项会被忽略。

> [!NOTE]
> 未卸载时在同一个 stdout 上重复调用 `render()` 不受支持。若需修改该选项或创建新实例，请先调用 `unmount()`。

```jsx
render(<MyApp />, {alternateScreen: true});
```

###### kittyKeyboard

Type: `object` 
Default: `undefined`

启用 [kitty keyboard protocol](https://sw.kovidgoyal.net/kitty/keyboard-protocol/) 以增强键盘输入处理。启用后，支持该协议的终端会报告更多按键信息，包括 `super`、`hyper`、`capsLock`、`numLock` 修饰键，以及 `eventType`（press/repeat/release）。

```jsx
import {render} from 'ink';

render(<MyApp />, {kittyKeyboard: {mode: 'auto'}});
```

```jsx
import {render} from 'ink';

render(<MyApp />, {
	kittyKeyboard: {
		mode: 'enabled',
		flags: ['disambiguateEscapeCodes', 'reportEventTypes'],
	},
});
```

**kittyKeyboard.mode**

Type: `'auto' | 'enabled' | 'disabled'` 
Default: `'auto'`

- `'auto'`: 先用启发式预检查（已知终端如 kitty、WezTerm、Ghostty）再做协议查询确认（`CSI ? u`）。仅当终端在短超时内响应查询时才启用协议。
- `'enabled'`: 强制启用协议。stdin 与 stdout 都必须是 TTY。
- `'disabled'`: 永不启用协议。

**kittyKeyboard.flags**

Type: `string[]` 
Default: `['disambiguateEscapeCodes']`

向终端请求的协议标志。传入标志名字符串数组。

可用标志：

- `'disambiguateEscapeCodes'` - 消除转义码歧义
- `'reportEventTypes'` - 报告按键按下、重复和释放事件
- `'reportAlternateKeys'` - 报告备用按键编码
- `'reportAllKeysAsEscapeCodes'` - 将所有按键作为转义码上报
- `'reportAssociatedText'` - 报告与按键事件关联的文本

**Behavior notes**

启用 kitty keyboard 协议后，输入处理在多个方面会发生变化：

- **非可打印键会产生空 input。** 功能键（F1-F35）、仅修饰键（Shift、Control、Super）、媒体键、Caps Lock、Print Screen 等不会在 `useInput` 的 `input` 参数中产生文本。但它们仍可通过 `key` 对象属性检测。
- **Ctrl+字母快捷键行为正确。** 当终端将 `Ctrl+字母` 以 codepoint 1-26（kitty CSI-u 的 alternate form）发送时，`input` 会被设置为对应字母（例如 `Ctrl+C` 为 `'c'`），且 `key.ctrl` 为 `true`。这保证无论终端采用哪种 codepoint 形式，`exitOnCtrlC` 和自定义 `Ctrl+字母` 处理都可持续工作。
- **按键去歧义。** 该协议允许终端区分通常会产生同一转义序列的按键。例如：
  - `Ctrl+I` 与 `Tab` - 不使用协议时，两者都产生同一字节（` x09`）；使用协议后会被区分为不同按键。
  - `Shift+Enter` 与 `Enter` - 可正确报告 shift 修饰键。
  - `Escape` 键与 `Ctrl+[` - 可以被区分。
- **事件类型。** 配合 `reportEventTypes` 标志，可通过 `key.eventType` 区分按下、重复与释放。

#### renderToString(tree, options?)

Returns: `string`

将 React 元素同步渲染为字符串。与 `render()` 不同，此函数不会写入 stdout，不会建立任何终端事件监听，并直接返回渲染结果字符串。

适用于生成文档、写文件、测试，或任何你需要字符串输出而不希望启动持久终端应用的场景。

```jsx
import {renderToString, Text, Box} from 'ink';

const output = renderToString(
	<Box padding={1}>
		<Text color="green">Hello World</Text>
	</Box>,
);

console.log(output);
```

**Notes:**

- 终端相关 Hook（`useInput`、`useStdin`、`useStdout`、`useStderr`、`useWindowSize`、`useApp`、`useFocus`、`useFocusManager`）会返回默认 no-op 值，因为此时没有终端会话。它们不会抛错，但行为不会与真实终端一致。
- `useEffect` 回调会在渲染期间执行（由于同步渲染模式），但其触发的状态更新不会影响返回结果；返回值反映的是初始渲染。
- `useLayoutEffect` 回调会在提交阶段同步执行，因此其触发的状态更新**会**反映到输出中。
- `<Static>` 组件被支持，其输出会被前置到动态输出之前。
- 若组件在渲染期间抛错，清理完成后错误会继续向调用方抛出。

##### tree

Type: `ReactNode`

##### options

Type: `object`

###### columns

Type: `number` 
Default: `80`

虚拟终端宽度（列数），用于控制文本换行位置。

```jsx
const output = renderToString(<Text>{'A'.repeat(100)}</Text>, {
	columns: 40,
});
// Text wraps at 40 columns
```

#### Instance

这是 `render()` 返回的对象。

##### rerender(tree)

用新的根节点替换旧根节点，或更新当前根节点的 props。

###### tree

Type: `ReactNode`

```jsx
// Update props of the root node
const {rerender} = render(<Counter count={1} />);
rerender(<Counter count={2} />);

// Replace root node
const {rerender} = render(<OldCounter />);
rerender(<NewCounter />);
```

##### unmount()

手动卸载整个 Ink 应用。

```jsx
const {unmount} = render(<MyApp />);
unmount();
```

##### waitUntilExit()

Returns a promise that settles when the app is unmounted.

它会以 `exit(value)` 传入的值 resolve，并在 `exit(error)` 传入错误时 reject。
当手动调用 `unmount()` 时，它会在与卸载相关的 stdout 写入完成后才 settle。

```jsx
const {unmount, waitUntilExit} = render(<MyApp />);

setTimeout(unmount, 1000);

await waitUntilExit(); // 在调用 `unmount()` 后 resolve
```

##### waitUntilRenderFlush()

返回一个 Promise，会在待处理渲染输出刷新到 stdout 后 settle。

当你需要在某一帧真正写出后再运行代码时，这很有用：

```jsx
const {rerender, waitUntilRenderFlush} = render(<MyApp step="loading" />);

rerender(<MyApp step="ready" />);
await waitUntilRenderFlush(); // "ready" 对应输出已刷新

runNextCommand();
```

##### cleanup()

卸载当前应用，并删除与当前 `stdout` 关联的内部 Ink 实例。
这主要用于高级场景（例如测试），当你需要 `render()` 在同一流上创建全新实例时。
与直接删除内部实例不同，该方法还会清理终端状态（例如备用屏幕）。

##### clear()

清空输出。

```jsx
const {clear} = render(<MyApp />);
clear();
```

#### measureElement(ref)

测量指定 `<Box>` 元素的尺寸。
返回一个包含 `width` 和 `height` 属性的对象。
当组件需要获知可用空间大小时，这个函数非常有用。你可以在需要根据内容长度调整布局时使用它。

> [!NOTE]
> 在渲染期间（布局尚未计算完成前）调用 `measureElement()` 会返回 `{width: 0, height: 0}`。请在渲染后代码中调用它，例如 `useEffect`、`useLayoutEffect`、输入处理器或定时器回调。当内容变化时，请把相关依赖传给 effect，以便每次更新后重新测量。

##### ref

Type: `MutableRef`

通过 `ref` 属性获取到的 `<Box>` 元素引用。
关于如何获取引用，见 [Refs](https://reactjs.org/docs/refs-and-the-dom.html)。

```jsx
import {render, measureElement, Box, Text} from 'ink';

const Example = () => {
	const ref = useRef();

	useEffect(() => {
		const {width, height} = measureElement(ref.current);
		// width = 100, height = 1
	}, []);

	return (
		<Box width={100}>
			<Box ref={ref}>
				<Text>This box will stretch to 100 width</Text>
			</Box>
		</Box>
	);
};

render(<Example />);
```

## Testing

使用 [ink-testing-library](https://github.com/vadimdemedes/ink-testing-library) 可以非常方便地测试 Ink 组件。
下面是一个简单示例，用于检查组件渲染结果：

```jsx
import React from 'react';
import {Text} from 'ink';
import {render} from 'ink-testing-library';

const Test = () => <Text>Hello World</Text>;
const {lastFrame} = render(<Test />);

lastFrame() === 'Hello World'; //=> true
```

更多示例和完整文档请查看 [ink-testing-library](https://github.com/vadimdemedes/ink-testing-library)。

## Using React Devtools

![](media/devtools.jpg)

Ink 原生支持 [React Devtools](https://github.com/facebook/react/tree/master/packages/react-devtools)。
要在基于 Ink 的 CLI 中启用 React Devtools 集成，请先确保安装可选依赖 `react-devtools-core`，然后通过 `DEV=true` 环境变量运行你的应用：

```sh
DEV=true my-cli
```

然后启动 React Devtools：

```sh
npx react-devtools
```

启动后，你应能看到 CLI 的组件树。
你甚至可以检查并修改组件 props，并立即在 CLI 中看到效果，无需重启。

> [!NOTE]
> 测试结束后，你需要通过 <kbd>Ctrl</kbd>+<kbd>C</kbd> 手动退出 CLI。

## Screen Reader Support

Ink 提供了基础的屏幕阅读器支持。

要启用它，你可以向 `render` 函数传入 `isScreenReaderEnabled` 选项，或将环境变量 `INK_SCREEN_READER` 设为 `true`。

Ink 实现了 [ARIA 规范](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA) 的一小部分能力。

```jsx
render(<MyApp />, {isScreenReaderEnabled: true});
```

启用屏幕阅读器支持后，Ink 会尽可能生成对屏幕阅读器友好的输出。

例如，对于以下代码：

```jsx
<Box aria-role="checkbox" aria-state={{checked: true}}>
	<Text>Accept terms and conditions</Text>
</Box>
```

Ink 会为屏幕阅读器生成如下输出：

```
(checked) checkbox: Accept terms and conditions
```

如果你希望给屏幕阅读器展示不同内容，也可以提供自定义标签。

例如，在构建进度条时，可以使用 `aria-label` 为屏幕阅读器提供更具描述性的标签。

```jsx
<Box>
	<Box width="50%" height={1} backgroundColor="green" />
	<Text aria-label="Progress: 50%">50%</Text>
</Box>
```

在上面的示例中，屏幕阅读器会读出 "Progress: 50%"，而不是 "50%"。

### `aria-label`

Type: `string`

元素的屏幕阅读器标签。

### `aria-hidden`

Type: `boolean` 
Default: `false`

对屏幕阅读器隐藏该元素。

##### aria-role

Type: `string`

元素角色。

支持值：

- `button`
- `checkbox`
- `radio`
- `radiogroup`
- `list`
- `listitem`
- `menu`
- `menuitem`
- `progressbar`
- `tab`
- `tablist`
- `timer`
- `toolbar`
- `table`

##### aria-state

Type: `object`

元素状态。

支持值：

- `checked` (boolean)
- `disabled` (boolean)
- `expanded` (boolean)
- `selected` (boolean)

## Creating Components

在构建自定义组件时，务必重视可访问性。虽然 Ink 提供了构建基础能力，但确保组件可访问，能让更广泛的用户群体使用你的 CLI。

### General Principles

- **提供对屏幕阅读器友好的输出：** 使用 `useIsScreenReaderEnabled` Hook 检测屏幕阅读器是否启用，然后为其用户渲染更具描述性的输出。
- **善用 ARIA 属性：** 对具有明确角色的组件（例如复选框或按钮），在 `<Box>` 与 `<Text>` 上使用 `aria-role`、`aria-state` 和 `aria-label` 属性，为屏幕阅读器提供语义信息。

一个构建可访问组件的实践示例见 [ARIA example](/examples/aria/aria.tsx)。

## Useful Components

- [ink-text-input](https://github.com/vadimdemedes/ink-text-input) - 文本输入。
- [ink-spinner](https://github.com/vadimdemedes/ink-spinner) - 加载旋转器。
- [ink-select-input](https://github.com/vadimdemedes/ink-select-input) - 选择（下拉）输入。
- [ink-link](https://github.com/sindresorhus/ink-link) - 链接。
- [ink-gradient](https://github.com/sindresorhus/ink-gradient) - 渐变色。
- [ink-big-text](https://github.com/sindresorhus/ink-big-text) - 艺术大字。
- [ink-picture](https://github.com/endernoke/ink-picture) - 显示图片。
- [ink-tab](https://github.com/jdeniau/ink-tab) - 标签页。
- [ink-color-pipe](https://github.com/LitoMore/ink-color-pipe) - 用更简洁的样式字符串创建彩色文本。
- [ink-multi-select](https://github.com/karaggeorge/ink-multi-select) - 从列表中选择一个或多个值
- [ink-divider](https://github.com/JureSotosek/ink-divider) - 分隔线。
- [ink-progress-bar](https://github.com/brigand/ink-progress-bar) - 进度条。
- [ink-table](https://github.com/maticzav/ink-table) - 表格。
- [ink-ascii](https://github.com/hexrcs/ink-ascii) - 基于 Figlet、支持更多字体选择的艺术字组件。
- [ink-markdown](https://github.com/cameronhunter/ink-markdown) - 渲染带语法高亮的 Markdown。
- [ink-quicksearch-input](https://github.com/Eximchain/ink-quicksearch-input) - 带快速搜索导航的选择组件。
- [ink-confirm-input](https://github.com/kevva/ink-confirm-input) - Yes/No 确认输入。
- [ink-syntax-highlight](https://github.com/vsashyn/ink-syntax-highlight) - 代码语法高亮。
- [ink-form](https://github.com/lukasbach/ink-form) - 表单。
- [ink-task-list](https://github.com/privatenumber/ink-task-list) - 任务列表。
- [ink-spawn](https://github.com/kraenhansen/ink-spawn) - 启动子进程。
- [ink-titled-box](https://github.com/mishieck/ink-titled-box) - 带标题的 Box。
- [ink-chart](https://github.com/pppp606/ink-chart) - 火花线与柱状图。
- [ink-scroll-view](https://github.com/ByteLandTechnology/ink-scroll-view) - 滚动容器。
- [ink-scroll-list](https://github.com/ByteLandTechnology/ink-scroll-list) - 可滚动列表。
- [ink-stepper](https://github.com/archcorsair/ink-stepper) - 分步向导。
- [ink-virtual-list](https://github.com/archcorsair/ink-virtual-list) - 仅渲染可见项的虚拟列表，以提升性能。
- [ink-color-picker](https://github.com/sina-byn/ink-color-picker) - 颜色选择器。

## Useful Hooks

- [ink-use-stdout-dimensions](https://github.com/cameronhunter/ink-monorepo/tree/master/packages/ink-use-stdout-dimensions) - 订阅 stdout 尺寸。

## Recipes

- [Routing with React Router](recipes/routing.md) - 使用 `MemoryRouter` 在路由间导航。

## Examples

[`examples`](/examples) 目录包含一组真实示例。可通过以下命令运行：

```bash
npm run example examples/[example name]
# e.g. npm run example examples/borders
```

- [Jest](examples/jest/jest.tsx) - 基础 Jest UI 实现。
- [Counter](examples/counter/counter.tsx) - 每 100ms 递增一次的简单计数器。
- [Form with validation](https://github.com/final-form/rff-cli-example) - 使用 [Final Form](https://github.com/final-form/final-form#-final-form) 管理表单状态。
- [Borders](examples/borders/borders.tsx) - 为 `<Box>` 组件添加边框。
- [Suspense](examples/suspense/suspense.tsx) - 使用 React Suspense。
- [Table](examples/table/table.tsx) - 渲染多列多行表格。
- [Focus management](examples/use-focus/use-focus.tsx) - 使用 `useFocus` Hook 管理组件间焦点。
- [User input](examples/use-input/use-input.tsx) - 监听用户输入。
- [Write to stdout](examples/use-stdout/use-stdout.tsx) - 写入 stdout，绕过 Ink 主输出。
- [Write to stderr](examples/use-stderr/use-stderr.tsx) - 写入 stderr，绕过 Ink 主输出。
- [Static](examples/static/static.tsx) - 使用 `<Static>` 组件渲染永久输出。
- [Child process](examples/subprocess-output) - 渲染子进程输出。
- [Router](examples/router/router.tsx) - 使用 React Router 的 `MemoryRouter` 在路由间导航。

## Continuous Integration

在 CI 环境中运行时（通过 `CI` 环境变量检测），Ink 会调整其渲染行为：

- 退出时仅渲染最后一帧，而不是持续更新终端。这是因为多数 CI 环境不支持用于覆盖先前输出的 ANSI 转义序列。
- 不监听终端尺寸变化事件。

如果你的 CI 环境支持完整终端渲染，并且你希望禁用上述行为，请设置 `CI=false`：

```sh
CI=false node my-cli.js
```

## Maintainers

- [Vadim Demedes](https://github.com/vadimdemedes)
- [Sindre Sorhus](https://github.com/sindresorhus)
