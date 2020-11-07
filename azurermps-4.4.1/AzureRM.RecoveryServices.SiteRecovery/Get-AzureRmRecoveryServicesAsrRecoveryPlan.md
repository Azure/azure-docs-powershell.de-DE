---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: a10f7ffb1b05474e5d2b86fa7d7a55f825aaad25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664999"
---
# <span data-ttu-id="30643-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="30643-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="30643-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30643-102">SYNOPSIS</span></span>
<span data-ttu-id="30643-103">Ruft einen Wiederherstellungsplan oder alle Wiederherstellungspläne im Speicher für Wiederherstellungsdienste ab</span><span class="sxs-lookup"><span data-stu-id="30643-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30643-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30643-104">SYNTAX</span></span>

### <span data-ttu-id="30643-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="30643-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan [<CommonParameters>]
```

### <span data-ttu-id="30643-106">ByName</span><span class="sxs-lookup"><span data-stu-id="30643-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>] [<CommonParameters>]
```

### <span data-ttu-id="30643-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="30643-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>] [<CommonParameters>]
```

## <span data-ttu-id="30643-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30643-108">DESCRIPTION</span></span>
<span data-ttu-id="30643-109">Mit dem Cmdlet **Get-AzureRmRecoveryServicesAsrRecoveryPlan werden** die Details des angegebenen Wiederherstellungsplans oder aller Wiederherstellungspläne im Vault für Wiederherstellungsdienste abgerufen.</span><span class="sxs-lookup"><span data-stu-id="30643-109">The **Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="30643-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30643-110">EXAMPLES</span></span>

### <span data-ttu-id="30643-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="30643-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="30643-112">Ruft den Wiederherstellungsplan mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="30643-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="30643-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="30643-113">PARAMETERS</span></span>

### <span data-ttu-id="30643-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="30643-114">-FriendlyName</span></span>
<span data-ttu-id="30643-115">Gibt den Anzeigenamen des Wiederherstellungsplans an, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="30643-115">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="30643-116">-Name</span><span class="sxs-lookup"><span data-stu-id="30643-116">-Name</span></span>
<span data-ttu-id="30643-117">Gibt den Namen des abzurufenden Wiederherstellungsplans an.</span><span class="sxs-lookup"><span data-stu-id="30643-117">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="30643-118">-Path</span><span class="sxs-lookup"><span data-stu-id="30643-118">-Path</span></span>
<span data-ttu-id="30643-119">Gibt den Dateipfad an, zu dem dieses Cmdlet die JSON-Definition für den Wiederherstellungsplan speichert.</span><span class="sxs-lookup"><span data-stu-id="30643-119">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="30643-120">Die JSON-Definition kann bearbeitet werden, um den Wiederherstellungsplan zu ändern und den Wiederherstellungsplan über das Update-AzureRmRecoveryServicesASRRecoveryPlan-Cmdlet zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="30643-120">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="30643-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30643-121">CommonParameters</span></span>
<span data-ttu-id="30643-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30643-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30643-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30643-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30643-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30643-124">INPUTS</span></span>

### <span data-ttu-id="30643-125">Keine</span><span class="sxs-lookup"><span data-stu-id="30643-125">None</span></span>

## <span data-ttu-id="30643-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30643-126">OUTPUTS</span></span>

### <span data-ttu-id="30643-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="30643-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="30643-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="30643-128">NOTES</span></span>

## <span data-ttu-id="30643-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30643-129">RELATED LINKS</span></span>

[<span data-ttu-id="30643-130">Neu – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="30643-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="30643-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="30643-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="30643-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="30643-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
