---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358936"
---
# <span data-ttu-id="fe82d-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="fe82d-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="fe82d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe82d-102">SYNOPSIS</span></span>
<span data-ttu-id="fe82d-103">Listet alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="fe82d-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="fe82d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe82d-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fe82d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe82d-105">DESCRIPTION</span></span>
<span data-ttu-id="fe82d-106">Listet alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="fe82d-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="fe82d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe82d-107">EXAMPLES</span></span>

### <span data-ttu-id="fe82d-108">Beispiel 1: Erhalten der MySql-Serverreplikate nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="fe82d-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="fe82d-109">Dieses Cmdlet ruft die MySql-Serverreplikate nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="fe82d-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="fe82d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe82d-110">PARAMETERS</span></span>

### <span data-ttu-id="fe82d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe82d-111">-DefaultProfile</span></span>
<span data-ttu-id="fe82d-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe82d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe82d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe82d-113">-ResourceGroupName</span></span>
<span data-ttu-id="fe82d-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fe82d-114">The name of the resource group.</span></span>
<span data-ttu-id="fe82d-115">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="fe82d-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fe82d-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fe82d-116">-ServerName</span></span>
<span data-ttu-id="fe82d-117">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="fe82d-117">The name of the server.</span></span>

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

### <span data-ttu-id="fe82d-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe82d-118">-SubscriptionId</span></span>
<span data-ttu-id="fe82d-119">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="fe82d-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fe82d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe82d-120">CommonParameters</span></span>
<span data-ttu-id="fe82d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe82d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe82d-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe82d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe82d-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe82d-123">INPUTS</span></span>

## <span data-ttu-id="fe82d-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe82d-124">OUTPUTS</span></span>

### <span data-ttu-id="fe82d-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="fe82d-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="fe82d-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fe82d-126">NOTES</span></span>

<span data-ttu-id="fe82d-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="fe82d-127">ALIASES</span></span>

## <span data-ttu-id="fe82d-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fe82d-128">RELATED LINKS</span></span>

