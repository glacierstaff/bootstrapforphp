1. php artisan make:seeder AdminSeeder

2. 
<?php

namespace Database\Seeders;


use Illuminate\Database\Console\Seeds\WithoutModelEvents;
use Illuminate\Database\Seeder;
use App\Models\User; 
use Illuminate\Support\Facades\Hash; 

class AdminSeeder extends Seeder
{
    public function run(): void
    {
        User::create([
            'nik' => '2410',
            'name' => 'pearce',
            'username' => 'okta',
            'position' => 'Admin',
            'number_phone' => '081234567890',
            'password' => Hash::make('ganteng'),
            'role' => 'admin',
        ]);
    }
}

3. php artisan db:seed --class=AdminSeeder