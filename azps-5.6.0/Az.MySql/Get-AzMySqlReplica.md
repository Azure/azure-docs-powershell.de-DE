---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: d4579ec17d870c1f002ce40309aa580226ff143d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924032"
---
# <span data-ttu-id="45765-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="45765-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="45765-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45765-102">SYNOPSIS</span></span>
<span data-ttu-id="45765-103">Listen Sie alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="45765-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="45765-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45765-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="45765-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45765-105">DESCRIPTION</span></span>
<span data-ttu-id="45765-106">Listen Sie alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="45765-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="45765-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="45765-107">EXAMPLES</span></span>

### <span data-ttu-id="45765-108">Beispiel 1: Holen Sie sich das MySql-Serverreplikate nach Ressourcengruppe und Servername.</span><span class="sxs-lookup"><span data-stu-id="45765-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="45765-109">Dieses Cmdlet ruft das MySql-Serverreplikate nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="45765-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="45765-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="45765-110">PARAMETERS</span></span>

### <span data-ttu-id="45765-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45765-111">-DefaultProfile</span></span>
<span data-ttu-id="45765-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45765-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45765-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45765-113">-ResourceGroupName</span></span>
<span data-ttu-id="45765-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="45765-114">The name of the resource group.</span></span>
<span data-ttu-id="45765-115">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="45765-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="45765-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="45765-116">-ServerName</span></span>
<span data-ttu-id="45765-117">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="45765-117">The name of the server.</span></span>

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

### <span data-ttu-id="45765-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45765-118">-SubscriptionId</span></span>
<span data-ttu-id="45765-119">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="45765-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="45765-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45765-120">CommonParameters</span></span>
<span data-ttu-id="45765-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45765-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45765-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45765-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45765-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="45765-123">INPUTS</span></span>

## <span data-ttu-id="45765-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="45765-124">OUTPUTS</span></span>

### <span data-ttu-id="45765-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="45765-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="45765-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="45765-126">NOTES</span></span>

<span data-ttu-id="45765-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="45765-127">ALIASES</span></span>

## <span data-ttu-id="45765-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="45765-128">RELATED LINKS</span></span>

