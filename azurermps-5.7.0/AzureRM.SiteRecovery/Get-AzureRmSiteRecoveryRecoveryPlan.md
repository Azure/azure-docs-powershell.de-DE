---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3B879056-5BF3-4262-8BAA-E79589149370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: ae5a1d5a70064b3849bc8f38cab46ecfabaf4968
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664187"
---
# <span data-ttu-id="07391-101">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07391-101">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="07391-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07391-102">SYNOPSIS</span></span>
<span data-ttu-id="07391-103">Ruft einen Wiederherstellungsplan in der Websitewiederherstellung ab.</span><span class="sxs-lookup"><span data-stu-id="07391-103">Gets a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07391-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07391-104">SYNTAX</span></span>

### <span data-ttu-id="07391-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="07391-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07391-106">ByName</span><span class="sxs-lookup"><span data-stu-id="07391-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07391-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="07391-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07391-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07391-108">DESCRIPTION</span></span>
<span data-ttu-id="07391-109">Das Cmdlet " **Get-AzureRmSiteRecoveryRecoveryPlan** " Ruft einen Wiederherstellungsplan in Azure Site Recovery ab.</span><span class="sxs-lookup"><span data-stu-id="07391-109">The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="07391-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07391-110">EXAMPLES</span></span>

## <span data-ttu-id="07391-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="07391-111">PARAMETERS</span></span>

### <span data-ttu-id="07391-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07391-112">-DefaultProfile</span></span>
<span data-ttu-id="07391-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07391-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07391-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="07391-114">-FriendlyName</span></span>
<span data-ttu-id="07391-115">Gibt den Anzeigenamen des Wiederherstellungsplans an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="07391-115">Specifies the friendly name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="07391-116">-Name</span><span class="sxs-lookup"><span data-stu-id="07391-116">-Name</span></span>
<span data-ttu-id="07391-117">Gibt den Namen des Wiederherstellungsplans an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="07391-117">Specifies the name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="07391-118">-Path</span><span class="sxs-lookup"><span data-stu-id="07391-118">-Path</span></span>
<span data-ttu-id="07391-119">Gibt den Dateipfad an, zu dem dieses Cmdlet den Wiederherstellungsplan speichert.</span><span class="sxs-lookup"><span data-stu-id="07391-119">Specifies the file path to which this cmdlet saves the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07391-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07391-120">CommonParameters</span></span>
<span data-ttu-id="07391-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07391-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07391-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07391-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07391-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07391-123">INPUTS</span></span>

### <span data-ttu-id="07391-124">Keine</span><span class="sxs-lookup"><span data-stu-id="07391-124">None</span></span>
<span data-ttu-id="07391-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="07391-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07391-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07391-126">OUTPUTS</span></span>

### <span data-ttu-id="07391-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPlan]</span><span class="sxs-lookup"><span data-stu-id="07391-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan]</span></span>

## <span data-ttu-id="07391-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="07391-128">NOTES</span></span>

## <span data-ttu-id="07391-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07391-129">RELATED LINKS</span></span>

[<span data-ttu-id="07391-130">Neu – AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07391-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="07391-131">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07391-131">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="07391-132">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07391-132">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
