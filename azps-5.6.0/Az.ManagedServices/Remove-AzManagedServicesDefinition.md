---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 20c025399197f780331f6281c05f243744544c41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921155"
---
# <span data-ttu-id="9f079-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="9f079-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="9f079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f079-102">SYNOPSIS</span></span>
<span data-ttu-id="9f079-103">Löscht die Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="9f079-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="9f079-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f079-104">SYNTAX</span></span>

### <span data-ttu-id="9f079-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f079-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition [-Scope <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f079-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9f079-106">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f079-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f079-107">DESCRIPTION</span></span>
<span data-ttu-id="9f079-108">Löscht die Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="9f079-108">Deletes the registration definition.</span></span>

## <span data-ttu-id="9f079-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f079-109">EXAMPLES</span></span>

### <span data-ttu-id="9f079-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9f079-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502
PS C:\>
```

<span data-ttu-id="9f079-111">Entfernt die Registrierungsdefinition nach Name im Standardbereich.</span><span class="sxs-lookup"><span data-stu-id="9f079-111">Removes the registration definition by name at the default scope.</span></span>

### <span data-ttu-id="9f079-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9f079-112">Example 2</span></span>
```
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d
PS C:\> Remove-AzManagedServicesDefinition -InputObject $definition
PS C:\>
```

<span data-ttu-id="9f079-113">Löscht die Registrierungsdefinition, die dem Eingabeobjekt gegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9f079-113">Deletes the registration definition given the input object.</span></span>

## <span data-ttu-id="9f079-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9f079-114">PARAMETERS</span></span>

### <span data-ttu-id="9f079-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f079-115">-DefaultProfile</span></span>
<span data-ttu-id="9f079-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f079-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f079-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f079-117">-InputObject</span></span>
<span data-ttu-id="9f079-118">Das Registrierungsdefinitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="9f079-118">The registration definition object.</span></span>

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

### <span data-ttu-id="9f079-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9f079-119">-Name</span></span>
<span data-ttu-id="9f079-120">Der eindeutige Name der Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="9f079-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f079-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="9f079-121">-Scope</span></span>
<span data-ttu-id="9f079-122">Der Bereich, in dem die Registrierungsdefinition erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9f079-122">The scope where the registration definition created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f079-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9f079-123">-Confirm</span></span>
<span data-ttu-id="9f079-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f079-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f079-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f079-125">-WhatIf</span></span>
<span data-ttu-id="9f079-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f079-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f079-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f079-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f079-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f079-128">CommonParameters</span></span>
<span data-ttu-id="9f079-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f079-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f079-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f079-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f079-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f079-131">INPUTS</span></span>

### <span data-ttu-id="9f079-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="9f079-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="9f079-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f079-133">OUTPUTS</span></span>

### <span data-ttu-id="9f079-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="9f079-134">System.Void</span></span>
## <span data-ttu-id="9f079-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9f079-135">NOTES</span></span>

## <span data-ttu-id="9f079-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9f079-136">RELATED LINKS</span></span>
