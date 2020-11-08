---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
ms.openlocfilehash: 9342ea2486c28a44ba7ff4a22f21619846ac7010
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165624"
---
# <span data-ttu-id="4c252-101">Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4c252-101">Set-AzRoleAssignment</span></span>

## <span data-ttu-id="4c252-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c252-102">SYNOPSIS</span></span>
<span data-ttu-id="4c252-103">Aktualisieren einer vorhandenen Rollenzuweisung</span><span class="sxs-lookup"><span data-stu-id="4c252-103">Update an existing Role Assignment.</span></span>

## <span data-ttu-id="4c252-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c252-104">SYNTAX</span></span>

### <span data-ttu-id="4c252-105">RoleAssignmentParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4c252-105">RoleAssignmentParameterSet (Default)</span></span>
```
Set-AzRoleAssignment -InputObject <PSRoleAssignment> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c252-106">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c252-106">InputFileParameterSet</span></span>
```
Set-AzRoleAssignment -InputFile <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c252-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c252-107">DESCRIPTION</span></span>
<span data-ttu-id="4c252-108">Verwenden Sie den Befehl New-AzRoleAssignment, um eine vorhandene Aufgabe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4c252-108">Use the New-AzRoleAssignment command to modify an existing assignment.</span></span>  
<span data-ttu-id="4c252-109">Beschreibungen können eine beliebige gültige Zeichenfolge sein, die Sie für die diferentiate verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c252-109">Descriptions can be any valid string, use that to diferentiate from one another.</span></span>  
<span data-ttu-id="4c252-110">Wenn Bedingung festgelegte Bedingung ist, muss Version auch festgesetzt werden, aber wenn Sie eine Bedingung aktualisieren, die nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4c252-110">if Condition is set Condition Version has to be set as well but if you're updating a Condition that is not necesary.</span></span>
<span data-ttu-id="4c252-111">Die Bedingungs Version kann von 1,0 auf 2,0 aktualisiert werden, kann aber nicht zurückgestuft werden.</span><span class="sxs-lookup"><span data-stu-id="4c252-111">Condition Version can be upgraded from 1.0 to 2.0 but it can't not be downgraded back.</span></span> <span data-ttu-id="4c252-112">Seien Sie vorsichtig, da 2,0 nicht mit 1,0 retrocompatible ist.</span><span class="sxs-lookup"><span data-stu-id="4c252-112">Be cautious as 2.0 is not retrocompatible with 1.0.</span></span>

## <span data-ttu-id="4c252-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c252-113">EXAMPLES</span></span>

### <span data-ttu-id="4c252-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4c252-114">Example 1</span></span>
```powershell
$ConditionVersion = "2.0"
  $Description = "This is a new role assignment for John"
  $Condition = "@Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'"

  $roleAssignment = Get-AzRoleAssignment -Scope "/subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg" -PrincipalId "0c0f6cdc-90dd-4664-83c0-a0d986c4c604"
  $roleAssignment.Description = $Description
  $roleAssignment.Condition = $Condition
  $roleAssignment.ConditionVersion = $ConditionVersion

  Set-AzRoleAssignment -InputObject $roleAssignment -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="4c252-115">Aktualisieren einer vorhandenen Rollenzuweisung durch Ändern eines Objekts</span><span class="sxs-lookup"><span data-stu-id="4c252-115">Update an existing role assignment by modifying an object</span></span>

### <span data-ttu-id="4c252-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4c252-116">Example 2</span></span>
```powershell
Set-AzRoleAssignment -InputFile "C:\RoleAssignments\example.json" -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="4c252-117">Aktualisieren einer vorhandenen Rollenzuweisung mithilfe einer Datei</span><span class="sxs-lookup"><span data-stu-id="4c252-117">Update an existing role assignment by using a file</span></span>

## <span data-ttu-id="4c252-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c252-118">PARAMETERS</span></span>

### <span data-ttu-id="4c252-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c252-119">-DefaultProfile</span></span>
<span data-ttu-id="4c252-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4c252-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c252-121">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="4c252-121">-InputFile</span></span>
<span data-ttu-id="4c252-122">Dateiname mit einer einzelnen Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="4c252-122">File name containing a single role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c252-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4c252-123">-InputObject</span></span>
<span data-ttu-id="4c252-124">Rollenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="4c252-124">Role Assignment.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c252-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c252-125">-PassThru</span></span>
<span data-ttu-id="4c252-126">Wenn angegeben, wird die aktualisierte Rollenzuweisung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c252-126">If specified, displays the updated role assignment</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c252-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4c252-127">-Confirm</span></span>
<span data-ttu-id="4c252-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c252-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c252-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c252-129">-WhatIf</span></span>
<span data-ttu-id="4c252-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c252-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c252-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c252-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c252-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c252-132">CommonParameters</span></span>
<span data-ttu-id="4c252-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c252-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c252-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c252-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c252-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c252-135">INPUTS</span></span>

### <span data-ttu-id="4c252-136">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4c252-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="4c252-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c252-137">OUTPUTS</span></span>

### <span data-ttu-id="4c252-138">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4c252-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="4c252-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c252-139">NOTES</span></span>

## <span data-ttu-id="4c252-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c252-140">RELATED LINKS</span></span>
