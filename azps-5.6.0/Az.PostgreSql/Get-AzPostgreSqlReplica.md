---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: c8fea3c7d0cfca227a69f83a76d73617d69106a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919480"
---
# <span data-ttu-id="17b54-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="17b54-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="17b54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17b54-102">SYNOPSIS</span></span>
<span data-ttu-id="17b54-103">Listen Sie alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="17b54-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="17b54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17b54-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="17b54-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17b54-105">DESCRIPTION</span></span>
<span data-ttu-id="17b54-106">Listen Sie alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="17b54-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="17b54-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17b54-107">EXAMPLES</span></span>

### <span data-ttu-id="17b54-108">Beispiel 1: Erhalten des PostgreSql-Serverreplikates nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="17b54-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="17b54-109">Dieses Cmdlet ruft das PostgreSql-Serverreplikate nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="17b54-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="17b54-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="17b54-110">PARAMETERS</span></span>

### <span data-ttu-id="17b54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b54-111">-DefaultProfile</span></span>
<span data-ttu-id="17b54-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17b54-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17b54-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17b54-113">-ResourceGroupName</span></span>
<span data-ttu-id="17b54-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="17b54-114">The name of the resource group.</span></span>
<span data-ttu-id="17b54-115">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="17b54-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="17b54-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="17b54-116">-ServerName</span></span>
<span data-ttu-id="17b54-117">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="17b54-117">The name of the server.</span></span>

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

### <span data-ttu-id="17b54-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17b54-118">-SubscriptionId</span></span>
<span data-ttu-id="17b54-119">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="17b54-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="17b54-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b54-120">CommonParameters</span></span>
<span data-ttu-id="17b54-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b54-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b54-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17b54-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b54-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17b54-123">INPUTS</span></span>

## <span data-ttu-id="17b54-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17b54-124">OUTPUTS</span></span>

### <span data-ttu-id="17b54-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="17b54-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="17b54-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="17b54-126">NOTES</span></span>

<span data-ttu-id="17b54-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="17b54-127">ALIASES</span></span>

## <span data-ttu-id="17b54-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="17b54-128">RELATED LINKS</span></span>

