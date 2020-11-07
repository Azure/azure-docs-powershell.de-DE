---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e313b3dd9df76185c1eeaf289e918e1d47ace58d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662220"
---
# <span data-ttu-id="07def-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="07def-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="07def-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07def-102">SYNOPSIS</span></span>
<span data-ttu-id="07def-103">Erstellt eine Zuordnung der ASR-Speicher Klassifikation im Recovery Services Vault.</span><span class="sxs-lookup"><span data-stu-id="07def-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07def-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07def-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07def-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07def-105">DESCRIPTION</span></span>
<span data-ttu-id="07def-106">Das Cmdlet **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** erstellt eine Speicher Klassifikation, die den Wiederherstellungsdienste-Tresor zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="07def-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="07def-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07def-107">EXAMPLES</span></span>

### <span data-ttu-id="07def-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="07def-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="07def-109">Startet den Speicher Klassifizierungs Zuordnungs Erstellungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="07def-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="07def-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="07def-110">PARAMETERS</span></span>

### <span data-ttu-id="07def-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="07def-111">-Confirm</span></span>
<span data-ttu-id="07def-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07def-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07def-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07def-113">-DefaultProfile</span></span>
<span data-ttu-id="07def-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07def-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="07def-115">-Name</span><span class="sxs-lookup"><span data-stu-id="07def-115">-Name</span></span>
<span data-ttu-id="07def-116">Gibt einen Namen für die ASR-Speicher Klassifikations Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="07def-116">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="07def-117">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="07def-117">-PrimaryStorageClassification</span></span>
<span data-ttu-id="07def-118">Gibt das primäre ASR-Speicher Klassifikations Objekt für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="07def-118">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07def-119">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="07def-119">-RecoveryStorageClassification</span></span>
<span data-ttu-id="07def-120">Gibt das Wiederherstellungs-ASR-Speicher Klassifikations Objekt für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="07def-120">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07def-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07def-121">-WhatIf</span></span>
<span data-ttu-id="07def-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07def-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07def-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07def-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07def-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07def-124">CommonParameters</span></span>
<span data-ttu-id="07def-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07def-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07def-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07def-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07def-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07def-127">INPUTS</span></span>

### <span data-ttu-id="07def-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="07def-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="07def-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07def-129">OUTPUTS</span></span>

### <span data-ttu-id="07def-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="07def-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="07def-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="07def-131">NOTES</span></span>

## <span data-ttu-id="07def-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07def-132">RELATED LINKS</span></span>

[<span data-ttu-id="07def-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="07def-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="07def-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="07def-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
