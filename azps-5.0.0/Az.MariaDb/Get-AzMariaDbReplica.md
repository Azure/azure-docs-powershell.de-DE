---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179111"
---
# <span data-ttu-id="c2246-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="c2246-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="c2246-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2246-102">SYNOPSIS</span></span>
<span data-ttu-id="c2246-103">Auflisten aller Replikate für einen bestimmten Server</span><span class="sxs-lookup"><span data-stu-id="c2246-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="c2246-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2246-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c2246-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2246-105">DESCRIPTION</span></span>
<span data-ttu-id="c2246-106">Auflisten aller Replikate für einen bestimmten Server</span><span class="sxs-lookup"><span data-stu-id="c2246-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="c2246-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2246-107">EXAMPLES</span></span>

### <span data-ttu-id="c2246-108">Beispiel 1: Auflisten aller Replikat-DB unter einem MariaDB</span><span class="sxs-lookup"><span data-stu-id="c2246-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c2246-109">Dieser Befehl listet alle Replikat-DB unter einem MariaDB auf.</span><span class="sxs-lookup"><span data-stu-id="c2246-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="c2246-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2246-110">PARAMETERS</span></span>

### <span data-ttu-id="c2246-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2246-111">-DefaultProfile</span></span>
<span data-ttu-id="c2246-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2246-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2246-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2246-113">-ResourceGroupName</span></span>
<span data-ttu-id="c2246-114">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c2246-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c2246-115">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="c2246-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c2246-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="c2246-116">-ServerName</span></span>
<span data-ttu-id="c2246-117">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="c2246-117">The name of the server.</span></span>

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

### <span data-ttu-id="c2246-118">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c2246-118">-SubscriptionId</span></span>
<span data-ttu-id="c2246-119">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c2246-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="c2246-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2246-120">CommonParameters</span></span>
<span data-ttu-id="c2246-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2246-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2246-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2246-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2246-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2246-123">INPUTS</span></span>

## <span data-ttu-id="c2246-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2246-124">OUTPUTS</span></span>

### <span data-ttu-id="c2246-125">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="c2246-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="c2246-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2246-126">NOTES</span></span>

<span data-ttu-id="c2246-127">Aliase</span><span class="sxs-lookup"><span data-stu-id="c2246-127">ALIASES</span></span>

## <span data-ttu-id="c2246-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2246-128">RELATED LINKS</span></span>

