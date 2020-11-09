---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: d4390f7de7b9fb91cf998050f192a3ba282e9585
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297064"
---
# <span data-ttu-id="9c53d-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="9c53d-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="9c53d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c53d-102">SYNOPSIS</span></span>
<span data-ttu-id="9c53d-103">Listenanfang Menüelemente in der angegebenen Anwendungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9c53d-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="9c53d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c53d-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9c53d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c53d-105">DESCRIPTION</span></span>
<span data-ttu-id="9c53d-106">Listenanfang Menüelemente in der angegebenen Anwendungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9c53d-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="9c53d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c53d-107">EXAMPLES</span></span>

### <span data-ttu-id="9c53d-108">Beispiel 2: Listenelemente des Windows Virtual Desktop-Start Menüs</span><span class="sxs-lookup"><span data-stu-id="9c53d-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="9c53d-109">Dieser Befehl listet die Start Menüelemente des Windows-virtuellen Desktops in einer Applicaton-Gruppe auf.</span><span class="sxs-lookup"><span data-stu-id="9c53d-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="9c53d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c53d-110">PARAMETERS</span></span>

### <span data-ttu-id="9c53d-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="9c53d-111">-ApplicationGroupName</span></span>
<span data-ttu-id="9c53d-112">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="9c53d-112">The name of the application group</span></span>

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

### <span data-ttu-id="9c53d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c53d-113">-DefaultProfile</span></span>
<span data-ttu-id="9c53d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c53d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c53d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c53d-115">-ResourceGroupName</span></span>
<span data-ttu-id="9c53d-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9c53d-116">The name of the resource group.</span></span>
<span data-ttu-id="9c53d-117">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="9c53d-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9c53d-118">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9c53d-118">-SubscriptionId</span></span>
<span data-ttu-id="9c53d-119">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="9c53d-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9c53d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c53d-120">CommonParameters</span></span>
<span data-ttu-id="9c53d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c53d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c53d-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c53d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c53d-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c53d-123">INPUTS</span></span>

## <span data-ttu-id="9c53d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c53d-124">OUTPUTS</span></span>

### <span data-ttu-id="9c53d-125">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="9c53d-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IStartMenuItem</span></span>

## <span data-ttu-id="9c53d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c53d-126">NOTES</span></span>

<span data-ttu-id="9c53d-127">Aliase</span><span class="sxs-lookup"><span data-stu-id="9c53d-127">ALIASES</span></span>

## <span data-ttu-id="9c53d-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c53d-128">RELATED LINKS</span></span>

