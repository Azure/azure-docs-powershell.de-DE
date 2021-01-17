---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
ms.openlocfilehash: 1f165177871a2d8b425829dddaef6d1f0298cfb4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356906"
---
# <span data-ttu-id="04bba-101">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="04bba-101">New-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="04bba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04bba-102">SYNOPSIS</span></span>
<span data-ttu-id="04bba-103">Erstellt eine neue vom Benutzer zugewiesene Identität oder aktualisiert eine vorhandene vom Benutzer zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="04bba-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

## <span data-ttu-id="04bba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04bba-104">SYNTAX</span></span>

```
New-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04bba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04bba-105">DESCRIPTION</span></span>
<span data-ttu-id="04bba-106">Das **Cmdlet "New-AzUserAssignedIdentity"** erstellt eine neue vom Benutzer zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="04bba-106">The **New-AzUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="04bba-107">Bei Verwendung mit einer bereits vorhandenen Identität wurde die Identität aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="04bba-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="04bba-108">Um der Identität Azure Resource Manager-Tags hinzuzufügen, verwenden Sie das Set-AzResource Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04bba-108">To add Azure Resource Manager tags to the identity, please use the Set-AzResource cmdlet.</span></span>

## <span data-ttu-id="04bba-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04bba-109">EXAMPLES</span></span>

### <span data-ttu-id="04bba-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="04bba-110">Example 1</span></span>
<span data-ttu-id="04bba-111">Dieses Beispiel-Cmdlet erstellt eine neue "Benutzer zugewiesene Identität" mit der **Namen-ID1** unter **"Ressourcengruppe PSRG"** am Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="04bba-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : centralus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="04bba-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="04bba-112">Example 2</span></span>
<span data-ttu-id="04bba-113">Mit diesem Beispiel-Cmdlet wird unter der Ressourcengruppe **"PSRG"** in der Region "westus" eine neue "Benutzer zugewiesene Identität" mit der **Namen-ID1** erstellt.</span><span class="sxs-lookup"><span data-stu-id="04bba-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="04bba-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04bba-114">PARAMETERS</span></span>

### <span data-ttu-id="04bba-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04bba-115">-AsJob</span></span>
<span data-ttu-id="04bba-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="04bba-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04bba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04bba-117">-DefaultProfile</span></span>
<span data-ttu-id="04bba-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04bba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04bba-119">-Location</span><span class="sxs-lookup"><span data-stu-id="04bba-119">-Location</span></span>
<span data-ttu-id="04bba-120">Der Name der Azure-Region, in dem die Identität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="04bba-120">The Azure region name where the Identity should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04bba-121">-Name</span><span class="sxs-lookup"><span data-stu-id="04bba-121">-Name</span></span>
<span data-ttu-id="04bba-122">Der Identitätsname.</span><span class="sxs-lookup"><span data-stu-id="04bba-122">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04bba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04bba-123">-ResourceGroupName</span></span>
<span data-ttu-id="04bba-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="04bba-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04bba-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="04bba-125">-Tag</span></span>
<span data-ttu-id="04bba-126">Die Azure Resource Manager-Tags, die der Identität zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="04bba-126">The Azure Resource Manager tags associated with the identity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04bba-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04bba-127">-Confirm</span></span>
<span data-ttu-id="04bba-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04bba-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04bba-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="04bba-129">-WhatIf</span></span>
<span data-ttu-id="04bba-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04bba-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04bba-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04bba-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04bba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04bba-132">CommonParameters</span></span>
<span data-ttu-id="04bba-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04bba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04bba-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04bba-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04bba-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04bba-135">INPUTS</span></span>

### <span data-ttu-id="04bba-136">System.String</span><span class="sxs-lookup"><span data-stu-id="04bba-136">System.String</span></span>

### <span data-ttu-id="04bba-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="04bba-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="04bba-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04bba-138">OUTPUTS</span></span>

### <span data-ttu-id="04bba-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="04bba-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="04bba-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="04bba-140">NOTES</span></span>

## <span data-ttu-id="04bba-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="04bba-141">RELATED LINKS</span></span>
