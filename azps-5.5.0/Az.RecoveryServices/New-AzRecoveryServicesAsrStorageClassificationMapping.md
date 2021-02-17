---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 091f8892238d88554d0e0c3502ffbeb8e8d4c154
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172218"
---
# <span data-ttu-id="61be2-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="61be2-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="61be2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61be2-102">SYNOPSIS</span></span>
<span data-ttu-id="61be2-103">Erstellt eine ASR-Speicherklassifizierungszuordnung im Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="61be2-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="61be2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61be2-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61be2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61be2-105">DESCRIPTION</span></span>
<span data-ttu-id="61be2-106">Das **Cmdlet "New-AzRecoveryServicesAsrStorageClassificationMapping"** erstellt eine Speicherklassifizierungszuordnung für den Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="61be2-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="61be2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="61be2-107">EXAMPLES</span></span>

### <span data-ttu-id="61be2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="61be2-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="61be2-109">Startet den Vorgang zum Erstellen der Speicherklassifizierungszuordnung mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="61be2-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="61be2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61be2-110">PARAMETERS</span></span>

### <span data-ttu-id="61be2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61be2-111">-DefaultProfile</span></span>
<span data-ttu-id="61be2-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61be2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="61be2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="61be2-113">-Name</span></span>
<span data-ttu-id="61be2-114">Gibt einen Namen für die Zuordnung der ASR-Speicherklassifizierung an.</span><span class="sxs-lookup"><span data-stu-id="61be2-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="61be2-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="61be2-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="61be2-116">Gibt das primäre AsR-Speicherklassifikationsobjekt für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="61be2-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="61be2-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="61be2-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="61be2-118">Gibt das Wiederherstellungs-ASR-Speicherklassifikationsobjekt für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="61be2-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="61be2-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61be2-119">-Confirm</span></span>
<span data-ttu-id="61be2-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61be2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61be2-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="61be2-121">-WhatIf</span></span>
<span data-ttu-id="61be2-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61be2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61be2-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61be2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61be2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61be2-124">CommonParameters</span></span>
<span data-ttu-id="61be2-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61be2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61be2-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61be2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61be2-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="61be2-127">INPUTS</span></span>

### <span data-ttu-id="61be2-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="61be2-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="61be2-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="61be2-129">OUTPUTS</span></span>

### <span data-ttu-id="61be2-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="61be2-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="61be2-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="61be2-131">NOTES</span></span>

## <span data-ttu-id="61be2-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="61be2-132">RELATED LINKS</span></span>

[<span data-ttu-id="61be2-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="61be2-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="61be2-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="61be2-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
