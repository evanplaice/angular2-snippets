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

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
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
    <th>description</th>
    <th>completion</th>
  </tr>
</table>

### Decorators

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
  </tr>
</table>

### Lifecycle

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
  </tr>
</table>

### Routing

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
  </tr>
</table>

### Directives

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
  </tr>
</table>

### Attributes

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
  </tr>
</table>

### Pipes

<table>
  <tr>
    <th>description</th>
    <th>completion</th>
  </tr>
</table>
