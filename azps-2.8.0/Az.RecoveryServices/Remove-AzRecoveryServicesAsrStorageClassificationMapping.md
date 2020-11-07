---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c76c2ebf40f360820ec3eef719b33142daacdbac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825248"
---
# <span data-ttu-id="42809-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="42809-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="42809-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42809-102">SYNOPSIS</span></span>
<span data-ttu-id="42809-103">Löscht die angegebene Zuordnung der ASR-Speicher Klassifikation.</span><span class="sxs-lookup"><span data-stu-id="42809-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="42809-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42809-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42809-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42809-105">DESCRIPTION</span></span>
<span data-ttu-id="42809-106">Das Cmdlet **Remove-AzRecoveryServicesAsrStorageClassificationMapping** löscht die angegebene Zuordnung der angegebenen Azure Site Recovery-Speicher Klassifikation.</span><span class="sxs-lookup"><span data-stu-id="42809-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="42809-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42809-107">EXAMPLES</span></span>

### <span data-ttu-id="42809-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42809-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="42809-109">Startet das Löschen der angegebenen Speicher Klassifikations Zuordnung und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42809-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="42809-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="42809-110">PARAMETERS</span></span>

### <span data-ttu-id="42809-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42809-111">-DefaultProfile</span></span>
<span data-ttu-id="42809-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42809-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="42809-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="42809-113">-InputObject</span></span>
<span data-ttu-id="42809-114">Das Eingabeobjekt für das Cmdlet: das ASR-Zuordnungsobjekt, das der zu löschenden ASR-Speicher Klassifikations Zuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="42809-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42809-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42809-115">-Confirm</span></span>
<span data-ttu-id="42809-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42809-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42809-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42809-117">-WhatIf</span></span>
<span data-ttu-id="42809-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42809-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42809-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42809-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42809-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42809-120">CommonParameters</span></span>
<span data-ttu-id="42809-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42809-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42809-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42809-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42809-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42809-123">INPUTS</span></span>

### <span data-ttu-id="42809-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="42809-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="42809-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42809-125">OUTPUTS</span></span>

### <span data-ttu-id="42809-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="42809-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="42809-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="42809-127">NOTES</span></span>

## <span data-ttu-id="42809-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42809-128">RELATED LINKS</span></span>

[<span data-ttu-id="42809-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="42809-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="42809-130">Neu – AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="42809-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
