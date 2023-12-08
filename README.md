# PHP

## :dart: Overview

###

<details>
<summary>:keyboard: Descrição</summary>

**:book: Tipos primitivos**

**:books: Estruturas de dados**

**:abacus: Operadores aritméticos**

**:floppy_disk: Operadores relacionais**

**:bulb: Operadores lógicos**

**:flashlight: Estruturas condicionais**

**:cd: Estruturas de repetição**

**:electric_plug: Funções**

**:page_with_curl: Classes**

**:mailbox_with_no_mail: Comandos**

</details>

<details>
<summary>:package: Laravel (Framework)</summary>

#### :keyboard: Descrição

- MVC: Model View Controller
- Actions: Ações dos controller acessando a model e renderizando as views
- Blade: Template engine laravel
- Path Params: Obrigatório ou opcional com uso '?'
- Query Params: Utilizado em campos de buscas
- Eloquent: ORM (Object-Relational Mapping)
- Migrations: Versionamento do banco de dados
- Flash Message: Passagem de mensagem por session
- Diretivas/Interpolação:

  ```
    @if(cond)
      ...
    @elseif(cond)
      ...
    @else
      ...
    @endif

    @for($i = 0; $i < count($arr), $i++)
      <p>{{ $arr[$i] }} - {{ $i }}</p>
    @endfor

    @foreach($arr as $var)
      <p>{{ $var }} - {{ $loop->index }}</p>
    @endforeach

    @php
      ...
    @endphp

    @yield('content')
    @yield('title')

    @extends('layouts.main')
    @section('title', 'Home')

    @section('content')
      ...
    @endsection

    @csrf
    @method("PUT")

    @auth
      ...
    @endauth

    @guest
      ...
    @endguest

    {{ $variable }}
    {{-- Comment --}}
  ```

- Comandos:

  ```
  composer create-project --prefer-dist laravel/laravel <project-name>
  composer require laravel/jetstream
  php artisan jetstream:install livewire

  php artisan serve

  php artisan migrate
  php artisan migrate:fresh
  php artisan migrate:status
  php artisan migrate:rollback
  php artisan migrate:reset
  php artisan migrate:refresh

  php artisan make:migration create_products_table
  php artisan make:migration add_category_to_products_table

  php artisan make:controller EventController
  php artisan make:model Event
  ```

</details>
