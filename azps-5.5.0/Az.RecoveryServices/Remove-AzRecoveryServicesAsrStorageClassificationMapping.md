---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8dcab2bcaeafbc5304de72b8bcf539a6f4a53934
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172200"
---
# <span data-ttu-id="3604f-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3604f-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="3604f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3604f-102">SYNOPSIS</span></span>
<span data-ttu-id="3604f-103">Löscht die angegebene Zuordnung der ASR-Speicherklassifizierung.</span><span class="sxs-lookup"><span data-stu-id="3604f-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="3604f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3604f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3604f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3604f-105">DESCRIPTION</span></span>
<span data-ttu-id="3604f-106">Das **Cmdlet "Remove-AzRecoveryServicesAsrStorageClassificationMapping"** löscht die angegebene Zuordnung der Azure Site Recovery-Speicherklassifizierung.</span><span class="sxs-lookup"><span data-stu-id="3604f-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="3604f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3604f-107">EXAMPLES</span></span>

### <span data-ttu-id="3604f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3604f-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="3604f-109">Startet das Löschen der angegebenen Speicherklassifizierungszuordnung und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="3604f-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3604f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3604f-110">PARAMETERS</span></span>

### <span data-ttu-id="3604f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3604f-111">-DefaultProfile</span></span>
<span data-ttu-id="3604f-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3604f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3604f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3604f-113">-InputObject</span></span>
<span data-ttu-id="3604f-114">Das Eingabeobjekt für das Cmdlet: Das ASR-Speicherklassifikationszuordnungsobjekt, das der zu löschende ASR-Speicherklassifizierungszuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="3604f-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="3604f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3604f-115">-Confirm</span></span>
<span data-ttu-id="3604f-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3604f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3604f-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3604f-117">-WhatIf</span></span>
<span data-ttu-id="3604f-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3604f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3604f-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3604f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3604f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3604f-120">CommonParameters</span></span>
<span data-ttu-id="3604f-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3604f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3604f-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3604f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3604f-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3604f-123">INPUTS</span></span>

### <span data-ttu-id="3604f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3604f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="3604f-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3604f-125">OUTPUTS</span></span>

### <span data-ttu-id="3604f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="3604f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3604f-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3604f-127">NOTES</span></span>

## <span data-ttu-id="3604f-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3604f-128">RELATED LINKS</span></span>

[<span data-ttu-id="3604f-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3604f-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="3604f-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3604f-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
