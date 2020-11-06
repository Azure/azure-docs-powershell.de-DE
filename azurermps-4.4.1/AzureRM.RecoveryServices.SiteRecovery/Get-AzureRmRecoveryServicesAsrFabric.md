---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: dde3873c7fe7ee18ee4745af967eb222833029d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478998"
---
# <span data-ttu-id="b86a0-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b86a0-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="b86a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b86a0-102">SYNOPSIS</span></span>
<span data-ttu-id="b86a0-103">Abrufen der Details eines Azure Site Recovery-Fabrics</span><span class="sxs-lookup"><span data-stu-id="b86a0-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b86a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b86a0-104">SYNTAX</span></span>

### <span data-ttu-id="b86a0-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="b86a0-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [<CommonParameters>]
```

### <span data-ttu-id="b86a0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b86a0-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="b86a0-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b86a0-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="b86a0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b86a0-108">DESCRIPTION</span></span>
<span data-ttu-id="b86a0-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrFabric** " Ruft die Eigenschaften eines angegebenen Azure Site Recovery-Fabrics oder aller Azure Site Recovery-Fabrics in einem Recovery Service Vault ab.</span><span class="sxs-lookup"><span data-stu-id="b86a0-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="b86a0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b86a0-110">EXAMPLES</span></span>

### <span data-ttu-id="b86a0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b86a0-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="b86a0-112">Gibt alle Azure Site Recovery-Fabrics im Tresor zurück.</span><span class="sxs-lookup"><span data-stu-id="b86a0-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

## <span data-ttu-id="b86a0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b86a0-113">PARAMETERS</span></span>

### <span data-ttu-id="b86a0-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b86a0-114">-FriendlyName</span></span>
<span data-ttu-id="b86a0-115">Suchen Sie nach dem ASR-Stoff anhand des Anzeigenamens des Stoffs.</span><span class="sxs-lookup"><span data-stu-id="b86a0-115">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b86a0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b86a0-116">-Name</span></span>
<span data-ttu-id="b86a0-117">Suchen Sie nach dem ASR-Stoff nach dem Namen des Stoffs.</span><span class="sxs-lookup"><span data-stu-id="b86a0-117">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b86a0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b86a0-118">CommonParameters</span></span>
<span data-ttu-id="b86a0-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b86a0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b86a0-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b86a0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b86a0-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b86a0-121">INPUTS</span></span>

### <span data-ttu-id="b86a0-122">Keine</span><span class="sxs-lookup"><span data-stu-id="b86a0-122">None</span></span>

## <span data-ttu-id="b86a0-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b86a0-123">OUTPUTS</span></span>

### <span data-ttu-id="b86a0-124">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b86a0-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b86a0-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="b86a0-125">NOTES</span></span>

## <span data-ttu-id="b86a0-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b86a0-126">RELATED LINKS</span></span>

[<span data-ttu-id="b86a0-127">Neu – AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b86a0-127">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="b86a0-128">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b86a0-128">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
