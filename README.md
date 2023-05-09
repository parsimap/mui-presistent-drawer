# Persistent Drawer

# Arguments

| argument     | type     | default     | description                           |
|--------------|----------|-------------|---------------------------------------|
| `openTitle`  | `string` | `undefined` | a title when drawer is need to opened |
| `closeTitle` | `string` | `undefined` | a title when drawer is need to closed |
| `width`      | `number` | `undefined` | to define width to drawer             |

## Optional Arguments

| argument       | type       | default     | description                            |
|----------------|------------|-------------|----------------------------------------|
| `scroll`       | `boolean`  | `false`     | to have scroll in drawer               |
| `right`        | `number`   | `undefined` | to move drawer to left                 |
| `top`          | `number`   | `undefined` | to move drawer to bottom               |
| `onOpenChange` | `function` | `undefined` | recognize when the drawer state change |

## Changelog

### Version: `1.0.5`

* The right property was added to a component to adapt that with another component on the right side of the main
  layout.
* The problem of is taken away button on page while parent own any position was resolved.
* The top property was added to a component.

### version: `1.0.6`

* The package name is renamed from mui-presistent-drawer to mui-persistent-drawer and corrected in the project.

### version `1.0.7`

* The documentation is rewrite in the case of separation the optional and required arguments.
* Add the ability to customizing title of the toggle button when it is opened or closed.

## Usage

```tsx
import MuiPersistentDrawer from '@parsimap/MuiPersistentDrawer';

const App = () => {
	function handleOpenChange(state: boolean) {
		if (state) {
			// Drawer is opend 
		}
	}

	return (
		<MuiPersistentDrawer
			width={400}
			openTitle={"Close Details"}
			closeTitle={"Close Details"}
			onOpenChange={handleOpenChange}
		/>
	)
}

export default App;
```