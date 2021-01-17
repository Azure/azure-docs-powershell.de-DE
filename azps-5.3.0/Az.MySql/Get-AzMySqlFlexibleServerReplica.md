---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 77b1dae0db73a9a90a2100edef893edabfe87d0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472283"
---
# <span data-ttu-id="dacb7-101">Get-AzMySqlFlexibleServerReplica</span><span class="sxs-lookup"><span data-stu-id="dacb7-101">Get-AzMySqlFlexibleServerReplica</span></span>

## <span data-ttu-id="dacb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dacb7-102">SYNOPSIS</span></span>
<span data-ttu-id="dacb7-103">Listet alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="dacb7-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="dacb7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dacb7-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dacb7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dacb7-105">DESCRIPTION</span></span>
<span data-ttu-id="dacb7-106">Listet alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="dacb7-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="dacb7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dacb7-107">EXAMPLES</span></span>

### <span data-ttu-id="dacb7-108">Beispiel 1: Erhalten der MySql-Serverreplikate nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="dacb7-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="dacb7-109">Dieses Cmdlet ruft die MySql-Serverreplikate nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="dacb7-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="dacb7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dacb7-110">PARAMETERS</span></span>

### <span data-ttu-id="dacb7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dacb7-111">-DefaultProfile</span></span>
<span data-ttu-id="dacb7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dacb7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dacb7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dacb7-113">-ResourceGroupName</span></span>
<span data-ttu-id="dacb7-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dacb7-114">The name of the resource group.</span></span>
<span data-ttu-id="dacb7-115">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="dacb7-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dacb7-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dacb7-116">-ServerName</span></span>
<span data-ttu-id="dacb7-117">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="dacb7-117">The name of the server.</span></span>

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

### <span data-ttu-id="dacb7-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dacb7-118">-SubscriptionId</span></span>
<span data-ttu-id="dacb7-119">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="dacb7-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dacb7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dacb7-120">CommonParameters</span></span>
<span data-ttu-id="dacb7-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dacb7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dacb7-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dacb7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dacb7-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dacb7-123">INPUTS</span></span>

## <span data-ttu-id="dacb7-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dacb7-124">OUTPUTS</span></span>

### <span data-ttu-id="dacb7-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="dacb7-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="dacb7-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dacb7-126">NOTES</span></span>

<span data-ttu-id="dacb7-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="dacb7-127">ALIASES</span></span>

## <span data-ttu-id="dacb7-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dacb7-128">RELATED LINKS</span></span>

