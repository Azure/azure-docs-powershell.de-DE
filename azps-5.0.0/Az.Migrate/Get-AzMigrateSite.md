---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179080"
---
# <span data-ttu-id="ec341-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="ec341-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="ec341-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec341-102">SYNOPSIS</span></span>
<span data-ttu-id="ec341-103">-Methode zum Abrufen einer Website.</span><span class="sxs-lookup"><span data-stu-id="ec341-103">Method to get a site.</span></span>

## <span data-ttu-id="ec341-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec341-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ec341-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec341-105">DESCRIPTION</span></span>
<span data-ttu-id="ec341-106">-Methode zum Abrufen einer Website.</span><span class="sxs-lookup"><span data-stu-id="ec341-106">Method to get a site.</span></span>

## <span data-ttu-id="ec341-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec341-107">EXAMPLES</span></span>

### <span data-ttu-id="ec341-108">Beispiel 1: Abrufen (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec341-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="ec341-109">Website nach Namen abrufen</span><span class="sxs-lookup"><span data-stu-id="ec341-109">Get site by name</span></span>

## <span data-ttu-id="ec341-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec341-110">PARAMETERS</span></span>

### <span data-ttu-id="ec341-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec341-111">-DefaultProfile</span></span>
<span data-ttu-id="ec341-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec341-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec341-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ec341-113">-Name</span></span>
<span data-ttu-id="ec341-114">Websitename</span><span class="sxs-lookup"><span data-stu-id="ec341-114">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec341-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec341-115">-ResourceGroupName</span></span>
<span data-ttu-id="ec341-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ec341-116">The name of the resource group.</span></span>
<span data-ttu-id="ec341-117">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ec341-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ec341-118">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="ec341-118">-SubscriptionId</span></span>
<span data-ttu-id="ec341-119">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="ec341-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ec341-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec341-120">CommonParameters</span></span>
<span data-ttu-id="ec341-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec341-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec341-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec341-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec341-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec341-123">INPUTS</span></span>

## <span data-ttu-id="ec341-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec341-124">OUTPUTS</span></span>

### <span data-ttu-id="ec341-125">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api202001. IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="ec341-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="ec341-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec341-126">NOTES</span></span>

<span data-ttu-id="ec341-127">Aliase</span><span class="sxs-lookup"><span data-stu-id="ec341-127">ALIASES</span></span>

## <span data-ttu-id="ec341-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec341-128">RELATED LINKS</span></span>

