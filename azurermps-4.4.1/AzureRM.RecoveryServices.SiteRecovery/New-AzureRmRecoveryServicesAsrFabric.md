---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 28c038a6dfd29f9daaeb942afa8fcb4c479cd0aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664732"
---
# <span data-ttu-id="0b94f-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="0b94f-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="0b94f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b94f-102">SYNOPSIS</span></span>
<span data-ttu-id="0b94f-103">Erstellt eine Azure Website-Wiederherstellungsstruktur.</span><span class="sxs-lookup"><span data-stu-id="0b94f-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b94f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b94f-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b94f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b94f-105">DESCRIPTION</span></span>
<span data-ttu-id="0b94f-106">Das Cmdlet **New-AzureRmRecoveryServicesAsrFabric** erstellt ein Azure Site Recovery-Fabric des angegebenen Typs.</span><span class="sxs-lookup"><span data-stu-id="0b94f-106">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="0b94f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b94f-107">EXAMPLES</span></span>

### <span data-ttu-id="0b94f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0b94f-108">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="0b94f-109">Startet die Fabric-Erstellung mit dem übergebenen Namen und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Fabric-Erstellungsvorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b94f-109">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="0b94f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b94f-110">PARAMETERS</span></span>

### <span data-ttu-id="0b94f-111">-Name</span><span class="sxs-lookup"><span data-stu-id="0b94f-111">-Name</span></span>
<span data-ttu-id="0b94f-112">Gibt den Namen des Azure Site Recovery-Fabrics an.</span><span class="sxs-lookup"><span data-stu-id="0b94f-112">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b94f-113">-Typ</span><span class="sxs-lookup"><span data-stu-id="0b94f-113">-Type</span></span>
<span data-ttu-id="0b94f-114">Gibt den Fabric-Typ "Azure Site Recovery" an.</span><span class="sxs-lookup"><span data-stu-id="0b94f-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b94f-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b94f-115">-Confirm</span></span>
<span data-ttu-id="0b94f-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b94f-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b94f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b94f-117">-WhatIf</span></span>
<span data-ttu-id="0b94f-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b94f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b94f-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b94f-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b94f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b94f-120">CommonParameters</span></span>
<span data-ttu-id="0b94f-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b94f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b94f-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b94f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b94f-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b94f-123">INPUTS</span></span>

### <span data-ttu-id="0b94f-124">Keine</span><span class="sxs-lookup"><span data-stu-id="0b94f-124">None</span></span>

## <span data-ttu-id="0b94f-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b94f-125">OUTPUTS</span></span>

### <span data-ttu-id="0b94f-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0b94f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0b94f-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b94f-127">NOTES</span></span>

## <span data-ttu-id="0b94f-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b94f-128">RELATED LINKS</span></span>

[<span data-ttu-id="0b94f-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="0b94f-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="0b94f-130">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="0b94f-130">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
