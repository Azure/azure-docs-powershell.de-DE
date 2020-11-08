---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179083"
---
# <span data-ttu-id="36bac-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="36bac-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="36bac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36bac-102">SYNOPSIS</span></span>
<span data-ttu-id="36bac-103">Die Methode zum Abrufen eines Ausführ Kontos.</span><span class="sxs-lookup"><span data-stu-id="36bac-103">Method to get run as account.</span></span>

## <span data-ttu-id="36bac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36bac-104">SYNTAX</span></span>

### <span data-ttu-id="36bac-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="36bac-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36bac-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="36bac-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="36bac-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36bac-107">DESCRIPTION</span></span>
<span data-ttu-id="36bac-108">Die Methode zum Abrufen eines Ausführ Kontos.</span><span class="sxs-lookup"><span data-stu-id="36bac-108">Method to get run as account.</span></span>

## <span data-ttu-id="36bac-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36bac-109">EXAMPLES</span></span>

### <span data-ttu-id="36bac-110">Beispiel 1: Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="36bac-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="36bac-111">Auflisten aller Ausführ als Konten auf einer Website</span><span class="sxs-lookup"><span data-stu-id="36bac-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="36bac-112">Beispiel 2: Abrufen</span><span class="sxs-lookup"><span data-stu-id="36bac-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="36bac-113">Führen Sie als Konto nach Namen.</span><span class="sxs-lookup"><span data-stu-id="36bac-113">Get Run as account by name.</span></span>

## <span data-ttu-id="36bac-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="36bac-114">PARAMETERS</span></span>

### <span data-ttu-id="36bac-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="36bac-115">-AccountName</span></span>
<span data-ttu-id="36bac-116">Führen Sie den Namen eines Konto Arms aus.</span><span class="sxs-lookup"><span data-stu-id="36bac-116">Run as account ARM name.</span></span>

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

### <span data-ttu-id="36bac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36bac-117">-DefaultProfile</span></span>
<span data-ttu-id="36bac-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36bac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36bac-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36bac-119">-ResourceGroupName</span></span>
<span data-ttu-id="36bac-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="36bac-120">The name of the resource group.</span></span>
<span data-ttu-id="36bac-121">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="36bac-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="36bac-122">-Sitename</span><span class="sxs-lookup"><span data-stu-id="36bac-122">-SiteName</span></span>
<span data-ttu-id="36bac-123">Websitename</span><span class="sxs-lookup"><span data-stu-id="36bac-123">Site name.</span></span>

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

### <span data-ttu-id="36bac-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="36bac-124">-SubscriptionId</span></span>
<span data-ttu-id="36bac-125">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="36bac-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="36bac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36bac-126">CommonParameters</span></span>
<span data-ttu-id="36bac-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36bac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36bac-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36bac-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36bac-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36bac-129">INPUTS</span></span>

## <span data-ttu-id="36bac-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36bac-130">OUTPUTS</span></span>

### <span data-ttu-id="36bac-131">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api202001. IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="36bac-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="36bac-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="36bac-132">NOTES</span></span>

<span data-ttu-id="36bac-133">Aliase</span><span class="sxs-lookup"><span data-stu-id="36bac-133">ALIASES</span></span>

## <span data-ttu-id="36bac-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36bac-134">RELATED LINKS</span></span>

