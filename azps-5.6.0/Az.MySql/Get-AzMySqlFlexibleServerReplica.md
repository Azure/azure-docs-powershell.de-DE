---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 25444df39945527d1bc574283e397407e0218633
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924035"
---
# <span data-ttu-id="2f933-101">Get-AzMySqlFlexibleServerReplica</span><span class="sxs-lookup"><span data-stu-id="2f933-101">Get-AzMySqlFlexibleServerReplica</span></span>

## <span data-ttu-id="2f933-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f933-102">SYNOPSIS</span></span>
<span data-ttu-id="2f933-103">Listen Sie alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="2f933-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="2f933-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f933-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2f933-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f933-105">DESCRIPTION</span></span>
<span data-ttu-id="2f933-106">Listen Sie alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="2f933-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="2f933-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2f933-107">EXAMPLES</span></span>

### <span data-ttu-id="2f933-108">Beispiel 1: Holen Sie sich das MySql-Serverreplikate nach Ressourcengruppe und Servername.</span><span class="sxs-lookup"><span data-stu-id="2f933-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="2f933-109">Dieses Cmdlet ruft das MySql-Serverreplikate nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="2f933-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="2f933-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2f933-110">PARAMETERS</span></span>

### <span data-ttu-id="2f933-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f933-111">-DefaultProfile</span></span>
<span data-ttu-id="2f933-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f933-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f933-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f933-113">-ResourceGroupName</span></span>
<span data-ttu-id="2f933-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2f933-114">The name of the resource group.</span></span>
<span data-ttu-id="2f933-115">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="2f933-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2f933-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="2f933-116">-ServerName</span></span>
<span data-ttu-id="2f933-117">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2f933-117">The name of the server.</span></span>

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

### <span data-ttu-id="2f933-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f933-118">-SubscriptionId</span></span>
<span data-ttu-id="2f933-119">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2f933-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2f933-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f933-120">CommonParameters</span></span>
<span data-ttu-id="2f933-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f933-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f933-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f933-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f933-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2f933-123">INPUTS</span></span>

## <span data-ttu-id="2f933-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2f933-124">OUTPUTS</span></span>

### <span data-ttu-id="2f933-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="2f933-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="2f933-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2f933-126">NOTES</span></span>

<span data-ttu-id="2f933-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2f933-127">ALIASES</span></span>

## <span data-ttu-id="2f933-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2f933-128">RELATED LINKS</span></span>

