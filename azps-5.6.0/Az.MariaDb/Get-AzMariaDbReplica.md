---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: c6fef537c3a0cc01bd2de01e00b69c1a69f81e3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927944"
---
# <span data-ttu-id="ebba1-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="ebba1-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="ebba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebba1-102">SYNOPSIS</span></span>
<span data-ttu-id="ebba1-103">Listen Sie alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="ebba1-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="ebba1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ebba1-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ebba1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebba1-105">DESCRIPTION</span></span>
<span data-ttu-id="ebba1-106">Listen Sie alle Replikate für einen bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="ebba1-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="ebba1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ebba1-107">EXAMPLES</span></span>

### <span data-ttu-id="ebba1-108">Beispiel 1: Auflisten aller Replikat-DB unter einer MariaDB</span><span class="sxs-lookup"><span data-stu-id="ebba1-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="ebba1-109">Mit diesem Befehl werden alle Replikat-DB unter einer MariaDB aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ebba1-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="ebba1-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ebba1-110">PARAMETERS</span></span>

### <span data-ttu-id="ebba1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebba1-111">-DefaultProfile</span></span>
<span data-ttu-id="ebba1-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ebba1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebba1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebba1-113">-ResourceGroupName</span></span>
<span data-ttu-id="ebba1-114">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="ebba1-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ebba1-115">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="ebba1-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ebba1-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="ebba1-116">-ServerName</span></span>
<span data-ttu-id="ebba1-117">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="ebba1-117">The name of the server.</span></span>

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

### <span data-ttu-id="ebba1-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ebba1-118">-SubscriptionId</span></span>
<span data-ttu-id="ebba1-119">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ebba1-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ebba1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebba1-120">CommonParameters</span></span>
<span data-ttu-id="ebba1-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebba1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebba1-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebba1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebba1-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ebba1-123">INPUTS</span></span>

## <span data-ttu-id="ebba1-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ebba1-124">OUTPUTS</span></span>

### <span data-ttu-id="ebba1-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="ebba1-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="ebba1-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ebba1-126">NOTES</span></span>

<span data-ttu-id="ebba1-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ebba1-127">ALIASES</span></span>

## <span data-ttu-id="ebba1-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ebba1-128">RELATED LINKS</span></span>

