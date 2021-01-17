---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369913"
---
# <span data-ttu-id="6732b-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="6732b-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="6732b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6732b-102">SYNOPSIS</span></span>
<span data-ttu-id="6732b-103">Methode zum Ausführen als Konto.</span><span class="sxs-lookup"><span data-stu-id="6732b-103">Method to get run as account.</span></span>

## <span data-ttu-id="6732b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6732b-104">SYNTAX</span></span>

### <span data-ttu-id="6732b-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="6732b-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6732b-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="6732b-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6732b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6732b-107">DESCRIPTION</span></span>
<span data-ttu-id="6732b-108">Methode zum Ausführen als Konto.</span><span class="sxs-lookup"><span data-stu-id="6732b-108">Method to get run as account.</span></span>

## <span data-ttu-id="6732b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6732b-109">EXAMPLES</span></span>

### <span data-ttu-id="6732b-110">Beispiel 1: Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="6732b-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="6732b-111">Alle als Konten auf einer Website ausgeführten Listen.</span><span class="sxs-lookup"><span data-stu-id="6732b-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="6732b-112">Beispiel 2: Erhalten</span><span class="sxs-lookup"><span data-stu-id="6732b-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="6732b-113">"Als Konto ausführen" nach Name.</span><span class="sxs-lookup"><span data-stu-id="6732b-113">Get Run as account by name.</span></span>

## <span data-ttu-id="6732b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6732b-114">PARAMETERS</span></span>

### <span data-ttu-id="6732b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6732b-115">-AccountName</span></span>
<span data-ttu-id="6732b-116">Als Kontonamen ARM ausführen.</span><span class="sxs-lookup"><span data-stu-id="6732b-116">Run as account ARM name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6732b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6732b-117">-DefaultProfile</span></span>
<span data-ttu-id="6732b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6732b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6732b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6732b-119">-ResourceGroupName</span></span>
<span data-ttu-id="6732b-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6732b-120">The name of the resource group.</span></span>
<span data-ttu-id="6732b-121">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="6732b-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6732b-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="6732b-122">-SiteName</span></span>
<span data-ttu-id="6732b-123">Websitename.</span><span class="sxs-lookup"><span data-stu-id="6732b-123">Site name.</span></span>

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

### <span data-ttu-id="6732b-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6732b-124">-SubscriptionId</span></span>
<span data-ttu-id="6732b-125">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="6732b-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6732b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6732b-126">CommonParameters</span></span>
<span data-ttu-id="6732b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6732b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6732b-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6732b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6732b-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6732b-129">INPUTS</span></span>

## <span data-ttu-id="6732b-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6732b-130">OUTPUTS</span></span>

### <span data-ttu-id="6732b-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="6732b-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="6732b-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6732b-132">NOTES</span></span>

<span data-ttu-id="6732b-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6732b-133">ALIASES</span></span>

## <span data-ttu-id="6732b-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6732b-134">RELATED LINKS</span></span>

