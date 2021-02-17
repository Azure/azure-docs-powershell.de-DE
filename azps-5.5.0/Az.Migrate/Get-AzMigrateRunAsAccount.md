---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152332"
---
# <span data-ttu-id="06606-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="06606-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="06606-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06606-102">SYNOPSIS</span></span>
<span data-ttu-id="06606-103">Methode zum Ausführen als Konto.</span><span class="sxs-lookup"><span data-stu-id="06606-103">Method to get run as account.</span></span>

## <span data-ttu-id="06606-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06606-104">SYNTAX</span></span>

### <span data-ttu-id="06606-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="06606-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="06606-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="06606-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="06606-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06606-107">DESCRIPTION</span></span>
<span data-ttu-id="06606-108">Methode zum Ausführen als Konto.</span><span class="sxs-lookup"><span data-stu-id="06606-108">Method to get run as account.</span></span>

## <span data-ttu-id="06606-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="06606-109">EXAMPLES</span></span>

### <span data-ttu-id="06606-110">Beispiel 1: Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="06606-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="06606-111">Alle als Konten auf einer Website ausgeführten Listen.</span><span class="sxs-lookup"><span data-stu-id="06606-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="06606-112">Beispiel 2: Erhalten</span><span class="sxs-lookup"><span data-stu-id="06606-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="06606-113">"Als Konto ausführen" nach Name.</span><span class="sxs-lookup"><span data-stu-id="06606-113">Get Run as account by name.</span></span>

## <span data-ttu-id="06606-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06606-114">PARAMETERS</span></span>

### <span data-ttu-id="06606-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="06606-115">-AccountName</span></span>
<span data-ttu-id="06606-116">Als Kontonamen ARM ausführen.</span><span class="sxs-lookup"><span data-stu-id="06606-116">Run as account ARM name.</span></span>

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

### <span data-ttu-id="06606-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06606-117">-DefaultProfile</span></span>
<span data-ttu-id="06606-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06606-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06606-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06606-119">-ResourceGroupName</span></span>
<span data-ttu-id="06606-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="06606-120">The name of the resource group.</span></span>
<span data-ttu-id="06606-121">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="06606-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="06606-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="06606-122">-SiteName</span></span>
<span data-ttu-id="06606-123">Websitename.</span><span class="sxs-lookup"><span data-stu-id="06606-123">Site name.</span></span>

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

### <span data-ttu-id="06606-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06606-124">-SubscriptionId</span></span>
<span data-ttu-id="06606-125">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="06606-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="06606-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06606-126">CommonParameters</span></span>
<span data-ttu-id="06606-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06606-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06606-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06606-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06606-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="06606-129">INPUTS</span></span>

## <span data-ttu-id="06606-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="06606-130">OUTPUTS</span></span>

### <span data-ttu-id="06606-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="06606-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="06606-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="06606-132">NOTES</span></span>

<span data-ttu-id="06606-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="06606-133">ALIASES</span></span>

## <span data-ttu-id="06606-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="06606-134">RELATED LINKS</span></span>

