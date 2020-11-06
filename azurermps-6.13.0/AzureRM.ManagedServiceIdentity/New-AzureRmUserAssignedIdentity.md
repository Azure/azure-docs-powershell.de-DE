---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/new-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/New-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/New-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: c0175c63a9e7a7d5df448d644783ac4b7a003e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495977"
---
# <span data-ttu-id="20378-101">New-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="20378-101">New-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="20378-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20378-102">SYNOPSIS</span></span>
<span data-ttu-id="20378-103">Erstellt einen neuen Benutzer, dem eine Identität zugewiesen wurde, oder aktualisiert eine vorhandene Benutzer zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="20378-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20378-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20378-104">SYNTAX</span></span>

```
New-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20378-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20378-105">DESCRIPTION</span></span>
<span data-ttu-id="20378-106">Das Cmdlet **New-AzureRmUserAssignedIdentity** erstellt eine neue Benutzer zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="20378-106">The **New-AzureRmUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="20378-107">Bei Verwendung mit einer bereits vorhandenen Identität wurde die Identität aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="20378-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="20378-108">Wenn Sie der Identität Azure Resource Manager-Tags hinzufügen möchten, verwenden Sie das Set-AzureRmResource-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20378-108">To add Azure Resource Manager tags to the identity, please use the Set-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="20378-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20378-109">EXAMPLES</span></span>

### <span data-ttu-id="20378-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20378-110">Example 1</span></span>
<span data-ttu-id="20378-111">Dieses Beispiel-Cmdlet erstellt einen neuen Benutzer, dem die Identität mit dem Namen **id1** unter Ressourcengruppe **PSRG** am Speicherort der ResourceGroup zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="20378-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzureRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

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

### <span data-ttu-id="20378-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="20378-112">Example 2</span></span>
<span data-ttu-id="20378-113">Dieses Beispiel-Cmdlet erstellt einen neuen Benutzer, dem eine Identität mit dem Namen **id1** unter der Ressourcengruppe **PSRG** in der Region westus zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="20378-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzureRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

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

## <span data-ttu-id="20378-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="20378-114">PARAMETERS</span></span>

### <span data-ttu-id="20378-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20378-115">-AsJob</span></span>
<span data-ttu-id="20378-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="20378-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20378-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20378-117">-DefaultProfile</span></span>
<span data-ttu-id="20378-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20378-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20378-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="20378-119">-Location</span></span>
<span data-ttu-id="20378-120">Der Name des Azure-Bereichs, in dem die Identität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="20378-120">The Azure region name where the Identity should be created.</span></span>

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

### <span data-ttu-id="20378-121">-Name</span><span class="sxs-lookup"><span data-stu-id="20378-121">-Name</span></span>
<span data-ttu-id="20378-122">Der Name der Identität.</span><span class="sxs-lookup"><span data-stu-id="20378-122">The Identity name.</span></span>

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

### <span data-ttu-id="20378-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20378-123">-ResourceGroupName</span></span>
<span data-ttu-id="20378-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="20378-124">The resource group name.</span></span>

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

### <span data-ttu-id="20378-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="20378-125">-Tag</span></span>
<span data-ttu-id="20378-126">Die Azure Resource Manager-Tags, die der Identität zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="20378-126">The Azure Resource Manager tags associated with the identity.</span></span>

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

### <span data-ttu-id="20378-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20378-127">-Confirm</span></span>
<span data-ttu-id="20378-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20378-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20378-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20378-129">-WhatIf</span></span>
<span data-ttu-id="20378-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20378-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20378-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20378-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20378-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20378-132">CommonParameters</span></span>
<span data-ttu-id="20378-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20378-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20378-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20378-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20378-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20378-135">INPUTS</span></span>

### <span data-ttu-id="20378-136">System. String</span><span class="sxs-lookup"><span data-stu-id="20378-136">System.String</span></span>

### <span data-ttu-id="20378-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="20378-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="20378-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20378-138">OUTPUTS</span></span>

### <span data-ttu-id="20378-139">Microsoft. Azure. Commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="20378-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="20378-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="20378-140">NOTES</span></span>

## <span data-ttu-id="20378-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20378-141">RELATED LINKS</span></span>
