---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: b19808ff7b5576c93bc81414d665e23086e524d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919184"
---
# <span data-ttu-id="20a5b-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="20a5b-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="20a5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="20a5b-103">Löscht die angegebene ASR-Speicherklassifizierungszuordnung.</span><span class="sxs-lookup"><span data-stu-id="20a5b-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="20a5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20a5b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20a5b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20a5b-105">DESCRIPTION</span></span>
<span data-ttu-id="20a5b-106">Das **Cmdlet Remove-AzRecoveryServicesAsrStorageClassificationMapping löscht** die angegebene Azure Site Recovery-Speicherklassifizierungszuordnung.</span><span class="sxs-lookup"><span data-stu-id="20a5b-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="20a5b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20a5b-107">EXAMPLES</span></span>

### <span data-ttu-id="20a5b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20a5b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="20a5b-109">Startet das Löschen der angegebenen Speicherklassifizierungszuordnung und gibt den ZUM Nachverfolgen des Vorgangs verwendeten ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="20a5b-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="20a5b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="20a5b-110">PARAMETERS</span></span>

### <span data-ttu-id="20a5b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a5b-111">-DefaultProfile</span></span>
<span data-ttu-id="20a5b-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20a5b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="20a5b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20a5b-113">-InputObject</span></span>
<span data-ttu-id="20a5b-114">Das Eingabeobjekt für das Cmdlet: Das ASR-Speicherklassifizierungszuordnungsobjekt, das der zu löschende ASR-Speicherklassifizierungszuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="20a5b-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="20a5b-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20a5b-115">-Confirm</span></span>
<span data-ttu-id="20a5b-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20a5b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20a5b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20a5b-117">-WhatIf</span></span>
<span data-ttu-id="20a5b-118">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20a5b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20a5b-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20a5b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20a5b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a5b-120">CommonParameters</span></span>
<span data-ttu-id="20a5b-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a5b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a5b-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20a5b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a5b-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20a5b-123">INPUTS</span></span>

### <span data-ttu-id="20a5b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="20a5b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="20a5b-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20a5b-125">OUTPUTS</span></span>

### <span data-ttu-id="20a5b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="20a5b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="20a5b-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="20a5b-127">NOTES</span></span>

## <span data-ttu-id="20a5b-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="20a5b-128">RELATED LINKS</span></span>

[<span data-ttu-id="20a5b-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="20a5b-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="20a5b-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="20a5b-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
