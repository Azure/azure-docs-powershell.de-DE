---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296787"
---
# <span data-ttu-id="c445a-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="c445a-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="c445a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c445a-102">SYNOPSIS</span></span>
<span data-ttu-id="c445a-103">Auflisten aller Replikate für einen bestimmten Server</span><span class="sxs-lookup"><span data-stu-id="c445a-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="c445a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c445a-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c445a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c445a-105">DESCRIPTION</span></span>
<span data-ttu-id="c445a-106">Auflisten aller Replikate für einen bestimmten Server</span><span class="sxs-lookup"><span data-stu-id="c445a-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="c445a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c445a-107">EXAMPLES</span></span>

### <span data-ttu-id="c445a-108">Beispiel 1: Abrufen des MySQL-Server Replikats nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="c445a-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="c445a-109">Dieses Cmdlet ruft das MySQL-Server Replikat nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="c445a-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="c445a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c445a-110">PARAMETERS</span></span>

### <span data-ttu-id="c445a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c445a-111">-DefaultProfile</span></span>
<span data-ttu-id="c445a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c445a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c445a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c445a-113">-ResourceGroupName</span></span>
<span data-ttu-id="c445a-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c445a-114">The name of the resource group.</span></span>
<span data-ttu-id="c445a-115">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="c445a-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c445a-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="c445a-116">-ServerName</span></span>
<span data-ttu-id="c445a-117">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="c445a-117">The name of the server.</span></span>

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

### <span data-ttu-id="c445a-118">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c445a-118">-SubscriptionId</span></span>
<span data-ttu-id="c445a-119">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c445a-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c445a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c445a-120">CommonParameters</span></span>
<span data-ttu-id="c445a-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c445a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c445a-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c445a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c445a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c445a-123">INPUTS</span></span>

## <span data-ttu-id="c445a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c445a-124">OUTPUTS</span></span>

### <span data-ttu-id="c445a-125">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="c445a-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="c445a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="c445a-126">NOTES</span></span>

<span data-ttu-id="c445a-127">Aliase</span><span class="sxs-lookup"><span data-stu-id="c445a-127">ALIASES</span></span>

## <span data-ttu-id="c445a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c445a-128">RELATED LINKS</span></span>

