---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302505"
---
# <span data-ttu-id="0af7b-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="0af7b-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="0af7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0af7b-102">SYNOPSIS</span></span>
<span data-ttu-id="0af7b-103">Ruft eine Liste der nicht aufgelösten Abhängigkeiten ab.</span><span class="sxs-lookup"><span data-stu-id="0af7b-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="0af7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0af7b-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0af7b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0af7b-105">DESCRIPTION</span></span>
<span data-ttu-id="0af7b-106">Ruft eine Liste der nicht aufgelösten Abhängigkeiten ab.</span><span class="sxs-lookup"><span data-stu-id="0af7b-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="0af7b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0af7b-107">EXAMPLES</span></span>

### <span data-ttu-id="0af7b-108">Beispiel 1: Abrufen einer Liste der unaufgelösten abhängigen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0af7b-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="0af7b-109">Abrufen einer Liste der nicht aufgelöst abhängigen Ressourcen für eine Move-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="0af7b-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="0af7b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0af7b-110">PARAMETERS</span></span>

### <span data-ttu-id="0af7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af7b-111">-DefaultProfile</span></span>
<span data-ttu-id="0af7b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0af7b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af7b-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="0af7b-113">-MoveCollectionName</span></span>
<span data-ttu-id="0af7b-114">Der Name der verschieben-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="0af7b-114">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af7b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af7b-115">-ResourceGroupName</span></span>
<span data-ttu-id="0af7b-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0af7b-116">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af7b-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="0af7b-117">-SubscriptionId</span></span>
<span data-ttu-id="0af7b-118">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0af7b-118">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0af7b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af7b-119">CommonParameters</span></span>
<span data-ttu-id="0af7b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0af7b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af7b-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0af7b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af7b-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0af7b-122">INPUTS</span></span>

## <span data-ttu-id="0af7b-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0af7b-123">OUTPUTS</span></span>

### <span data-ttu-id="0af7b-124">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="0af7b-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="0af7b-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="0af7b-125">NOTES</span></span>

<span data-ttu-id="0af7b-126">Aliase</span><span class="sxs-lookup"><span data-stu-id="0af7b-126">ALIASES</span></span>

## <span data-ttu-id="0af7b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0af7b-127">RELATED LINKS</span></span>

