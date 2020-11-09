---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303029"
---
# <span data-ttu-id="3e4c1-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="3e4c1-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="3e4c1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e4c1-102">SYNOPSIS</span></span>
<span data-ttu-id="3e4c1-103">Auflisten aller Replikate für einen bestimmten Server</span><span class="sxs-lookup"><span data-stu-id="3e4c1-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="3e4c1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e4c1-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3e4c1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e4c1-105">DESCRIPTION</span></span>
<span data-ttu-id="3e4c1-106">Auflisten aller Replikate für einen bestimmten Server</span><span class="sxs-lookup"><span data-stu-id="3e4c1-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="3e4c1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e4c1-107">EXAMPLES</span></span>

### <span data-ttu-id="3e4c1-108">Beispiel 1: Abrufen des PostgreSQL-Server Replikats nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="3e4c1-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3e4c1-109">Dieses Cmdlet ruft das Replikat des PostgreSQL-Servers nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="3e4c1-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="3e4c1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e4c1-110">PARAMETERS</span></span>

### <span data-ttu-id="3e4c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e4c1-111">-DefaultProfile</span></span>
<span data-ttu-id="3e4c1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3e4c1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e4c1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e4c1-113">-ResourceGroupName</span></span>
<span data-ttu-id="3e4c1-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3e4c1-114">The name of the resource group.</span></span>
<span data-ttu-id="3e4c1-115">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="3e4c1-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3e4c1-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="3e4c1-116">-ServerName</span></span>
<span data-ttu-id="3e4c1-117">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="3e4c1-117">The name of the server.</span></span>

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

### <span data-ttu-id="3e4c1-118">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="3e4c1-118">-SubscriptionId</span></span>
<span data-ttu-id="3e4c1-119">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="3e4c1-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3e4c1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e4c1-120">CommonParameters</span></span>
<span data-ttu-id="3e4c1-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e4c1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e4c1-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e4c1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e4c1-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e4c1-123">INPUTS</span></span>

## <span data-ttu-id="3e4c1-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e4c1-124">OUTPUTS</span></span>

### <span data-ttu-id="3e4c1-125">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="3e4c1-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="3e4c1-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e4c1-126">NOTES</span></span>

<span data-ttu-id="3e4c1-127">Aliase</span><span class="sxs-lookup"><span data-stu-id="3e4c1-127">ALIASES</span></span>

## <span data-ttu-id="3e4c1-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e4c1-128">RELATED LINKS</span></span>

