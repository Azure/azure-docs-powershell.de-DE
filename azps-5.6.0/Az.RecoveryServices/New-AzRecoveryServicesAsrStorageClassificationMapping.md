---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8ad9ca87687acfdeb526dc33cdcb5a6ec70c65bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919323"
---
# <span data-ttu-id="1a06c-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="1a06c-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="1a06c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a06c-102">SYNOPSIS</span></span>
<span data-ttu-id="1a06c-103">Erstellt eine ASR-Speicherklassifizierungszuordnung im Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="1a06c-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="1a06c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a06c-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a06c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a06c-105">DESCRIPTION</span></span>
<span data-ttu-id="1a06c-106">Das **Cmdlet New-AzRecoveryServicesAsrStorageClassificationMapping erstellt** eine Speicherklassifizierung, die den Recovery Services-Tresor zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1a06c-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="1a06c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a06c-107">EXAMPLES</span></span>

### <span data-ttu-id="1a06c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1a06c-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="1a06c-109">Startet den Erstellungsvorgang für die Speicherklassifizierungszuordnung mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1a06c-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1a06c-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1a06c-110">PARAMETERS</span></span>

### <span data-ttu-id="1a06c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a06c-111">-DefaultProfile</span></span>
<span data-ttu-id="1a06c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a06c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1a06c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1a06c-113">-Name</span></span>
<span data-ttu-id="1a06c-114">Gibt einen Namen für die ASR-Speicherklassifizierungszuordnung an.</span><span class="sxs-lookup"><span data-stu-id="1a06c-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="1a06c-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="1a06c-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="1a06c-116">Gibt das primäre ASR-Speicherklassifizierungsobjekt für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="1a06c-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="1a06c-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="1a06c-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="1a06c-118">Gibt das Wiederherstellungs-ASR-Speicherklassifizierungsobjekt für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="1a06c-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="1a06c-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1a06c-119">-Confirm</span></span>
<span data-ttu-id="1a06c-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a06c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a06c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a06c-121">-WhatIf</span></span>
<span data-ttu-id="1a06c-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a06c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a06c-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a06c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a06c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a06c-124">CommonParameters</span></span>
<span data-ttu-id="1a06c-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a06c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a06c-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a06c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a06c-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a06c-127">INPUTS</span></span>

### <span data-ttu-id="1a06c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="1a06c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="1a06c-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a06c-129">OUTPUTS</span></span>

### <span data-ttu-id="1a06c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="1a06c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1a06c-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1a06c-131">NOTES</span></span>

## <span data-ttu-id="1a06c-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1a06c-132">RELATED LINKS</span></span>

[<span data-ttu-id="1a06c-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="1a06c-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="1a06c-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="1a06c-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
