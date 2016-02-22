# Angular2 Snippets for Sublime Text

This package provides snippets and completions for Angular2. Sublime Text uses fuzzy searching for snippets/completions, therefore you can trigger either without having to write out the whole trigger.

## Installation

**Package Control**

- open the `Command Palette` (⌘ + ⇧ + p | SUPER + SHIFT + p)
- select `Package Control: Install Package` (p + i)
- select `Angular2 Snippets`

**Manual**

- copy/clone the files into your Sublime Text User Preferences folder

**Config**

- to enable auto-completion add the following to `User.sublime-preferences`

  ```json
  "auto_complete_triggers": [ {"selector": "text.html", "characters": "<"}, {"selector": "text.html meta.tag", "characters": " " } ]
  ```

## Directory

**Snippet Categories:**

- [Component](#component)
- [Directive](#directive)
- [Service](#service)
- [Pipe](#pipe)
- [RouteConfig](#routeconfig)
- [Route](#route)
- [Test](#test)

**Completion Categories:**

- [Annotations](#annotations)
- [Decorators](#decorators)
- [Lifecycle](#lifecycle)
- [Routing](#routing)
- [Directives](#directives)
- [Attributes](#attributes)
- [Pipes](#pipes)

## Snippets

### Component

**Trigger:** `component`

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
  </tr>
  <tr>
    <td>@Component</td>
    <td><pre style="padding:0; margin:0;"><code>
@Component(${2})
export class ${1}Component {${3}}
    </code></pre></td>
  </tr>
  <tr>
    <td>@Component (Basic)</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
@Component({
  selector: '${2}',
  template: '${3}',
  styles: '${4}'
})
export class ${1}Component {${5}}
    </code></pre></td>
  </tr>
  <tr>
    <td>@Component (External)</td>
    <td><pre style="padding:0; margin:0;"><code>
@Component({
  selector: '${2}',
  templateUrl: '${3}',
  styleUrls: ['${4}']
})
export class ${1}Component {${5}}
    </code></pre></td>
  </tr>
  <tr>
    <td>@Component (Complex)</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
@Component({
  selector: '${2}',
  providers: ['${3}'],
  viewProviders: ['${4}'],
  template: '${5}',
  templateUrl: '${6}',
  styles: '${7}',
  styleUrls: ['${8}'],
  directives: ['${9}'],
  pipes: ['${10}']
})
export class ${1}Component {${11}}
    </code></pre></td>
  </tr>
</table>

### Directive

**Trigger:** `directive`

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
  </tr>
  <tr>
    <td>@Directive</td>
    <td><pre style="padding:0; margin:0;"><code>
@Directive({${2}})
export class ${1}Directive {${3}}
    </code></pre></td>
  </tr>
  <tr>
    <td>@Directive (Basic)</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
@Directive({
  selector: '${2}'
})
export class ${1}Directive {${3}}
    </code></pre></td>
  </tr>
  <tr>
    <td>@Directive (Complex)</td>
    <td><pre style="padding:0; margin:0;"><code>
@Directive({
  selector: '${2}',
  providers: ['${3}'],
  properties: ['${4}'],
  host: {'${5}'}
})
export class ${1}Directive {${6}}
    </code></pre></td>
  </tr>
</table>

### Service

**Trigger:** `service`

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
  </tr>
  <tr>
    <td>Service</td>
    <td><pre style="padding:0; margin:0;"><code>
@Injectable()
export class ${1}Service {${2}}
    </code></pre></td>
  </tr>
</table>

### Pipe

**Trigger:** `pipe`

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
  </tr>
  <tr>
    <td>Pipe</td>
    <td><pre style="padding:0; margin:0;"><code>
@Pipe({ name: '${2}' })
export class ${1}Pipe implements PipeTransform {
  transform (value:number, args:${3:any}[]) : ${4:any} {${5}}
}
    </code></pre></td>
  </tr>
  <tr>
    <td>Pipe (ES6)</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
@Pipe({ name: '${2}' })
export class ${1}Pipe {
  transform (value, args) {${3}}
}
    </code></pre></td>
  </tr>
</table>

### RouteConfig

**Trigger:** `routeconfig`

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
  </tr>
  <tr>
    <td>@RouteConfig</td>
    <td><pre style="padding:0; margin:0;"><code>
@RouteConfig([
  ${1}
])
    </code></pre></td>
  </tr>
  <tr>
    <td>@RouteConfig (Basic)</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
@RouteConfig([
  {
    path: '/${1}',
    name: '${2}',
    component: ${2}Component,
    useAsDefault: true
  }${3}
]
    </code></pre></td>
  </tr>
</table>

### Route

**Trigger:** `route`

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
  </tr>
  <tr>
    <td>Route</td>
    <td><pre style="padding:0; margin:0;"><code>
{
  path: '/${1}',
  name: '${2}',
  component: ${2}Component
}${3}
    </code></pre></td>
  </tr>
  <tr>
    <td>Route (Default)</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
{
  path: '/${1}',
  name: '${2}',
  component: ${2}Component,
  useAsDefault: true
}${3}
    </code></pre></td>
  </tr>
  <tr>
    <td>Route (Redirect)</td>
    <td><pre style="padding:0; margin:0;"><code>
{
  path: '/${1:**}',
  redirectTo: ['${2}']
}${3}
    </code></pre></td>
  </tr>
  <tr>
    <td>Route (Param)</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
{
  path: '/${1}:${2}',
  name: '${3}',
  component: ${3}Component
}${4}
    </code></pre></td>
  </tr>
  <tr>
    <td>Route (Wildcard)</td>
    <td><pre style="padding:0; margin:0;"><code>
{
  path: '/${1}*${2}',
  name: '${3}',
  component: ${3}Component
}${4}
    </code></pre></td>
  </tr>
  <tr>
    <td>Route (Data)</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
{
  path: '/${1}',
  name: '${2}',
  component: ${2}Component,
  data: {${3}: ${4}}
}${5}
    </code></pre></td>
  </tr>
  <tr>
    <td>Route (Parent)</td>
    <td><pre style="padding:0; margin:0;"><code>
{
  path: '/${1}...',
  name: '${2}',
  component: ${2}Component
}${3}
    </code></pre></td>
  </tr>
</table>

### Test

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
  </tr>
</table>

## Completions

### Annotations

<table>
  <tr>
    <th>trigger</th>
    <th>completion</th>
  </tr>
  <tr>
    <td>selector</td>
    <td><pre style="padding:0; margin:0;"><code>
selector: '$1'
    </code></pre></td>
  </tr>
  <tr>
    <td>inputs</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
inputs: [
  '$1'
]
    </code></pre></td>
  </tr>
  <tr>
    <td>outputs</td>
    <td><pre style="padding:0; margin:0;"><code>
outputs: [
  '$1'
]
    </code></pre></td>
  </tr>
  <tr>
    <td>providers</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
providers: [
  $1
]
    </code></pre></td>
  </tr>
  <tr>
    <td>viewProviders</td>
    <td><pre style="padding:0; margin:0;"><code>
viewProviders: [
  $1
]
    </code></pre></td>
  </tr>
  <tr>
    <td>template</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
template: `
$1
`
    </code></pre></td>
  </tr>
  <tr>
    <td>templateUrl</td>
    <td><pre style="padding:0; margin:0;"><code>
templateUrl: '$1'
    </code></pre></td>
  </tr>
  <tr>
    <td>styles</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
styles: `
$1
`
    </code></pre></td>
  </tr>
  <tr>
    <td>styleUrls</td>
    <td><pre style="padding:0; margin:0;"><code>
styleUrls: [
  '$1'
]
    </code></pre></td>
  </tr>
  <tr>
    <td>directives</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
directives: [
  $1
]
    </code></pre></td>
  </tr>
  <tr>
    <td>pipes</td>
    <td><pre style="padding:0; margin:0;"><code>
pipes: [
  $1
]
    </code></pre></td>
  </tr>
  <tr>
    <td>properties</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
properties: [
  '$1'
]
    </code></pre></td>
  </tr>
  <tr>
    <td>host</td>
    <td><pre style="padding:0; margin:0;"><code>
host: {
  '$1': '$2'
}
    </code></pre></td>
  </tr>
</table>

### Decorators

<table>
  <tr>
    <th>trigger</th>
    <th>completion</th>
  </tr>
  <tr>
    <td>@Inject</td>
    <td><pre style="padding:0; margin:0;"><code>
@Inject($1) $2
    </code></pre></td>
  </tr>
  <tr>
    <td>@Input</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
@Input($1) $2
    </code></pre></td>
  </tr>
  <tr>
    <td>@Output</td>
    <td><pre style="padding:0; margin:0;"><code>
@Output($1) $2 = $3
    </code></pre></td>
  </tr>
  <tr>
    <td>@HostBinding</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
@HostBinding($1) $2
    </code></pre></td>
  </tr>
  <tr>
    <td>@HostListener</td>
    <td><pre style="padding:0; margin:0;"><code>
@HostListener('$1', ['$2'])
    </code></pre></td>
  </tr>
  <tr>
    <td>@ContentChild</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
@ContentChild($1)
    </code></pre></td>
  </tr>
  <tr>
    <td>@ContentChildren</td>
    <td><pre style="padding:0; margin:0;"><code>
@ContentChildren($1)
    </code></pre></td>
  </tr>
  <tr>
    <td>@ViewChild</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
@ViewChild($1)
    </code></pre></td>
  </tr>
  <tr>
    <td>@ViewChildren</td>
    <td><pre style="padding:0; margin:0;"><code>
@ViewChildren($1)
    </code></pre></td>
  </tr>
</table>

### Lifecycle

<table>
  <tr>
    <th>trigger</th>
    <th>completion</th>
  </tr>
  <tr>
    <td>constructor</td>
    <td><pre style="padding:0; margin:0;"><code>
constructor($1) {
  $2
}
    </code></pre></td>
  </tr>
  <tr>
    <td>ngOnChanges</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
ngOnChanges($1) {
  $2
}
    </code></pre></td>
  </tr>
  <tr>
    <td>ngOnInit</td>
    <td><pre style="padding:0; margin:0;"><code>
ngOnInit($1) {
  $2
}
    </code></pre></td>
  </tr>
  <tr>
    <td>ngDoCheck</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
ngDoCheck($1) {
  $2
}
    </code></pre></td>
  </tr>
  <tr>
    <td>ngAfterContentInit</td>
    <td><pre style="padding:0; margin:0;"><code>
ngAfterContentInit($1) {
  $2
}
    </code></pre></td>
  </tr>
  <tr>
    <td>ngAfterContentChecked</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
ngAfterContentChecked($1) {
  $2
}
    </code></pre></td>
  </tr>
  <tr>
    <td>ngAfterViewInit</td>
    <td><pre style="padding:0; margin:0;"><code>
ngAfterViewInit($1) {
  $2
}
    </code></pre></td>
  </tr>
  <tr>
    <td>ngAfterViewChecked</td>
    <td><pre style="padding:0; margin:0; background-color: #fff;"><code>
ngAfterViewChecked($1) {
  $2
}
    </code></pre></td>
  </tr>
  <tr>
    <td>ngOnDestroy</td>
    <td><pre style="padding:0; margin:0;"><code>
ngOnDestroy($1) {
  $2
}
    </code></pre></td>
  </tr>
</table>

### Routing

<table>
  <tr>
    <th>trigger</th>
    <th>completion</th>
  </tr>
</table>

### Directives

<table>
  <tr>
    <th>trigger</th>
    <th>completion</th>
  </tr>
</table>

### Attributes

<table>
  <tr>
    <th>trigger</th>
    <th>completion</th>
  </tr>
</table>

### Pipes

<table>
  <tr>
    <th>trigger</th>
    <th>completion</th>
  </tr>
</table>
