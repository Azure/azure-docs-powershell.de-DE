---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 8023dde9253ccb4a1f7ff223c4dfdddf773a4728
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467640"
---
# <span data-ttu-id="54b69-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="54b69-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="54b69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54b69-102">SYNOPSIS</span></span>
<span data-ttu-id="54b69-103">Erstellt oder aktualisiert eine Registrierungszuweisung.</span><span class="sxs-lookup"><span data-stu-id="54b69-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="54b69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54b69-104">SYNTAX</span></span>

### <span data-ttu-id="54b69-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="54b69-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54b69-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="54b69-106">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>]
 -RegistrationDefinition <PSRegistrationDefinition> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54b69-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54b69-107">DESCRIPTION</span></span>
<span data-ttu-id="54b69-108">Erstellt oder aktualisiert eine Registrierungszuweisung.</span><span class="sxs-lookup"><span data-stu-id="54b69-108">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="54b69-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54b69-109">EXAMPLES</span></span>

### <span data-ttu-id="54b69-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54b69-110">Example 1</span></span>
```
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded

PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\>
```

<span data-ttu-id="54b69-111">Erstellt eine Registrierungszuweisung im Standardbereich mithilfe des Registrierungsdefinitionsbezeichners.</span><span class="sxs-lookup"><span data-stu-id="54b69-111">Creates a registration assignment at the default scope using the registration definition identifier.</span></span>

### <span data-ttu-id="54b69-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="54b69-112">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b279ec53-b42f-4952-bd62-cd49982e9572 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/b279ec53-b42f-4952-bd62-cd49982e9572 Succeeded


PS C:\>
```

<span data-ttu-id="54b69-113">Erstellt eine Registrierungszuordnung mit einem Registrierungsdefinitionsobjekt als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="54b69-113">Creates a registration assignment with a registration definition object as input.</span></span>

### <span data-ttu-id="54b69-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="54b69-114">Example 3</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded

PS C:\>
```

<span data-ttu-id="54b69-115">Aktualisiert eine Registrierungszuweisung mit einem Registrierungsdefinitionsbezeichner und -namen.</span><span class="sxs-lookup"><span data-stu-id="54b69-115">Updates a registration assignment with a registration definition identifier and name.</span></span>


## <span data-ttu-id="54b69-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54b69-116">PARAMETERS</span></span>

### <span data-ttu-id="54b69-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b69-117">-DefaultProfile</span></span>
<span data-ttu-id="54b69-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54b69-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54b69-119">-Name</span><span class="sxs-lookup"><span data-stu-id="54b69-119">-Name</span></span>
<span data-ttu-id="54b69-120">Der eindeutige Name der Registrierungszuordnung.</span><span class="sxs-lookup"><span data-stu-id="54b69-120">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b69-121">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="54b69-121">-RegistrationDefinition</span></span>
<span data-ttu-id="54b69-122">Das Eingabeobjekt für die Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="54b69-122">The registration definition input object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54b69-123">-RegistrationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="54b69-123">-RegistrationDefinitionId</span></span>
<span data-ttu-id="54b69-124">Die vollqualifizierte Ressourcen-ID der Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="54b69-124">The fully qualified resource id of the registration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54b69-125">-Scope</span><span class="sxs-lookup"><span data-stu-id="54b69-125">-Scope</span></span>
<span data-ttu-id="54b69-126">Der Bereich, in dem die Registrierungszuordnung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="54b69-126">The scope where the registration assignment should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b69-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54b69-127">-AsJob</span></span>
<span data-ttu-id="54b69-128">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="54b69-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54b69-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54b69-129">-Confirm</span></span>
<span data-ttu-id="54b69-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54b69-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b69-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="54b69-131">-WhatIf</span></span>
<span data-ttu-id="54b69-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54b69-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54b69-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54b69-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b69-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b69-134">CommonParameters</span></span>
<span data-ttu-id="54b69-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54b69-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b69-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54b69-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b69-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54b69-137">INPUTS</span></span>

### <span data-ttu-id="54b69-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="54b69-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
### <span data-ttu-id="54b69-139">System.String</span><span class="sxs-lookup"><span data-stu-id="54b69-139">System.String</span></span>
## <span data-ttu-id="54b69-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54b69-140">OUTPUTS</span></span>

### <span data-ttu-id="54b69-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="54b69-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="54b69-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="54b69-142">NOTES</span></span>

## <span data-ttu-id="54b69-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="54b69-143">RELATED LINKS</span></span>
