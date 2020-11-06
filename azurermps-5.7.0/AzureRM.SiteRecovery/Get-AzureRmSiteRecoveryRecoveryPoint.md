---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77AFEF57-A4ED-4F82-A3FF-0E33D7810B3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
ms.openlocfilehash: 42a0a96a32bf1b7f556ee2787f43a5777afa1115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502402"
---
# <span data-ttu-id="4f657-101">Get-AzureRmSiteRecoveryRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4f657-101">Get-AzureRmSiteRecoveryRecoveryPoint</span></span>

## <span data-ttu-id="4f657-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f657-102">SYNOPSIS</span></span>
<span data-ttu-id="4f657-103">Ruft verfügbare Wiederherstellungspunkte für ein geschütztes Replikat Element ab.</span><span class="sxs-lookup"><span data-stu-id="4f657-103">Gets available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f657-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f657-104">SYNTAX</span></span>

### <span data-ttu-id="4f657-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f657-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f657-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4f657-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f657-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f657-107">DESCRIPTION</span></span>
<span data-ttu-id="4f657-108">Das Cmdlet " **Get-AzureRmSiteRecoveryRecoveryPoint** " Ruft die Liste der verfügbaren Wiederherstellungspunkte für ein geschütztes Replikations Element ab.</span><span class="sxs-lookup"><span data-stu-id="4f657-108">The **Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="4f657-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f657-109">EXAMPLES</span></span>

## <span data-ttu-id="4f657-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f657-110">PARAMETERS</span></span>

### <span data-ttu-id="4f657-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f657-111">-DefaultProfile</span></span>
<span data-ttu-id="4f657-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f657-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f657-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4f657-113">-Name</span></span>
<span data-ttu-id="4f657-114">Gibt den Namen des Wiederherstellungspunkts an, den das Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4f657-114">Specifies the name of the recovery point this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f657-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4f657-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="4f657-116">Gibt das Azure Site Recovery Replication Protected Item-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4f657-116">Specifies the Azure Site Recovery Replication Protected Item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f657-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f657-117">CommonParameters</span></span>
<span data-ttu-id="4f657-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f657-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f657-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f657-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f657-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f657-120">INPUTS</span></span>

### <span data-ttu-id="4f657-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4f657-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="4f657-122">Der Parameter "ReplicationProtectedItem" akzeptiert den Wert vom Typ "ASRReplicationProtectedItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4f657-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="4f657-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f657-123">OUTPUTS</span></span>

### <span data-ttu-id="4f657-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4f657-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4f657-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f657-125">NOTES</span></span>

## <span data-ttu-id="4f657-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f657-126">RELATED LINKS</span></span>

[<span data-ttu-id="4f657-127">Bearbeiten-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4f657-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Edit-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4f657-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4f657-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4f657-129">Neu – AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4f657-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4f657-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4f657-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="4f657-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4f657-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
