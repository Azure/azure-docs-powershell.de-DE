---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 091f8892238d88554d0e0c3502ffbeb8e8d4c154
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177893"
---
# <span data-ttu-id="f9bc7-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f9bc7-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="f9bc7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="f9bc7-103">Erstellt eine Zuordnung der ASR-Speicher Klassifikation im Recovery Services Vault.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="f9bc7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9bc7-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9bc7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9bc7-105">DESCRIPTION</span></span>
<span data-ttu-id="f9bc7-106">Das Cmdlet **New-AzRecoveryServicesAsrStorageClassificationMapping** erstellt eine Speicher Klassifikation, die den Wiederherstellungsdienste-Tresor zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="f9bc7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9bc7-107">EXAMPLES</span></span>

### <span data-ttu-id="f9bc7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f9bc7-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="f9bc7-109">Startet den Speicher Klassifizierungs Zuordnungs Erstellungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f9bc7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9bc7-110">PARAMETERS</span></span>

### <span data-ttu-id="f9bc7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9bc7-111">-DefaultProfile</span></span>
<span data-ttu-id="f9bc7-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9bc7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f9bc7-113">-Name</span></span>
<span data-ttu-id="f9bc7-114">Gibt einen Namen für die ASR-Speicher Klassifikations Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="f9bc7-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="f9bc7-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="f9bc7-116">Gibt das primäre ASR-Speicher Klassifikations Objekt für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bc7-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="f9bc7-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="f9bc7-118">Gibt das Wiederherstellungs-ASR-Speicher Klassifikations Objekt für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9bc7-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9bc7-119">-Confirm</span></span>
<span data-ttu-id="f9bc7-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9bc7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9bc7-121">-WhatIf</span></span>
<span data-ttu-id="f9bc7-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9bc7-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9bc7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9bc7-124">CommonParameters</span></span>
<span data-ttu-id="f9bc7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9bc7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9bc7-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9bc7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9bc7-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9bc7-127">INPUTS</span></span>

### <span data-ttu-id="f9bc7-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="f9bc7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="f9bc7-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9bc7-129">OUTPUTS</span></span>

### <span data-ttu-id="f9bc7-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f9bc7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f9bc7-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9bc7-131">NOTES</span></span>

## <span data-ttu-id="f9bc7-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9bc7-132">RELATED LINKS</span></span>

[<span data-ttu-id="f9bc7-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f9bc7-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="f9bc7-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f9bc7-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
