---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/get-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Get-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Get-AzUserAssignedIdentity.md
ms.openlocfilehash: 208997d6c51257aacdcb0dea14680be3fa042985
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650651"
---
# <span data-ttu-id="759f4-101">Get-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="759f4-101">Get-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="759f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="759f4-102">SYNOPSIS</span></span>
<span data-ttu-id="759f4-103">Ruft Benutzer zugewiesene Identitäten/Identitäten ab.</span><span class="sxs-lookup"><span data-stu-id="759f4-103">Gets User Assigned Identity/identities.</span></span>

## <span data-ttu-id="759f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="759f4-104">SYNTAX</span></span>

### <span data-ttu-id="759f4-105">SuscriptionParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="759f4-105">SuscriptionParameterSet (Default)</span></span>
```
Get-AzUserAssignedIdentity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="759f4-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="759f4-106">ResourceGroupParameterSet</span></span>
```
Get-AzUserAssignedIdentity -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="759f4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="759f4-107">DESCRIPTION</span></span>
<span data-ttu-id="759f4-108">Der **Get-AzUserAssignedIdentity** ruft vorhandene Benutzer zugewiesene Identitäten ab.</span><span class="sxs-lookup"><span data-stu-id="759f4-108">The **Get-AzUserAssignedIdentity** gets existing user assigned identities.</span></span>

## <span data-ttu-id="759f4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="759f4-109">EXAMPLES</span></span>

### <span data-ttu-id="759f4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="759f4-110">Example 1</span></span>
<span data-ttu-id="759f4-111">Dieses Beispiel-Cmdlet ruft die dem Benutzer zugewiesene Identität mit dem Namen **id1** unter der Ressourcengruppe **PSRG**</span><span class="sxs-lookup"><span data-stu-id="759f4-111">This example cmdlet gets the User Assigned Identity with name **ID1** under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

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

### <span data-ttu-id="759f4-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="759f4-112">Example 2</span></span>
<span data-ttu-id="759f4-113">Dieses Beispiel-Cmdlet ruft alle Benutzer zugewiesenen Identitäten unter der Ressourcengruppe **PSRG**</span><span class="sxs-lookup"><span data-stu-id="759f4-113">This example cmdlet gets all the User Assigned Identities under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzUserAssignedIdentity -ResourceGroupName PSRG

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="759f4-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="759f4-114">Example 3</span></span>
<span data-ttu-id="759f4-115">Dieses Beispiel-Cmdlet ruft alle Benutzer zugewiesenen Identitäten unter dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="759f4-115">This example cmdlet gets all the User Assigned Identities under the subscription.</span></span>

```powershell
PS C:\> Get-AzUserAssignedIdentity

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG2

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="759f4-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="759f4-116">PARAMETERS</span></span>

### <span data-ttu-id="759f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="759f4-117">-DefaultProfile</span></span>
<span data-ttu-id="759f4-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="759f4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="759f4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="759f4-119">-Name</span></span>
<span data-ttu-id="759f4-120">Der Name der Identität.</span><span class="sxs-lookup"><span data-stu-id="759f4-120">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759f4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="759f4-121">-ResourceGroupName</span></span>
<span data-ttu-id="759f4-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="759f4-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="759f4-123">CommonParameters</span></span>
<span data-ttu-id="759f4-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="759f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="759f4-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="759f4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="759f4-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="759f4-126">INPUTS</span></span>

### <span data-ttu-id="759f4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="759f4-127">System.String</span></span>

## <span data-ttu-id="759f4-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="759f4-128">OUTPUTS</span></span>

### <span data-ttu-id="759f4-129">Microsoft. Azure. Commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="759f4-129">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="759f4-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="759f4-130">NOTES</span></span>

## <span data-ttu-id="759f4-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="759f4-131">RELATED LINKS</span></span>
