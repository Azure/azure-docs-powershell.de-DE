---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298176"
---
# <span data-ttu-id="dbc89-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="dbc89-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="dbc89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbc89-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc89-103">Listet alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="dbc89-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="dbc89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbc89-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dbc89-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbc89-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc89-106">Listet alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="dbc89-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="dbc89-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dbc89-107">EXAMPLES</span></span>

### <span data-ttu-id="dbc89-108">Beispiel 1: Erhalten der PostgreSql-Serverreplikate nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="dbc89-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="dbc89-109">Dieses Cmdlet ruft die PostgreSql-Serverreplikate nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="dbc89-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="dbc89-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbc89-110">PARAMETERS</span></span>

### <span data-ttu-id="dbc89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc89-111">-DefaultProfile</span></span>
<span data-ttu-id="dbc89-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbc89-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbc89-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc89-113">-ResourceGroupName</span></span>
<span data-ttu-id="dbc89-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dbc89-114">The name of the resource group.</span></span>
<span data-ttu-id="dbc89-115">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="dbc89-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dbc89-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dbc89-116">-ServerName</span></span>
<span data-ttu-id="dbc89-117">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="dbc89-117">The name of the server.</span></span>

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

### <span data-ttu-id="dbc89-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dbc89-118">-SubscriptionId</span></span>
<span data-ttu-id="dbc89-119">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="dbc89-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dbc89-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc89-120">CommonParameters</span></span>
<span data-ttu-id="dbc89-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc89-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc89-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbc89-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc89-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dbc89-123">INPUTS</span></span>

## <span data-ttu-id="dbc89-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dbc89-124">OUTPUTS</span></span>

### <span data-ttu-id="dbc89-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="dbc89-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="dbc89-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dbc89-126">NOTES</span></span>

<span data-ttu-id="dbc89-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="dbc89-127">ALIASES</span></span>

## <span data-ttu-id="dbc89-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dbc89-128">RELATED LINKS</span></span>

