---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 3d26a5285fbe96c0e77c56819567e21820cddf4f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663545"
---
# <span data-ttu-id="3a83c-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3a83c-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="3a83c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a83c-102">SYNOPSIS</span></span>
<span data-ttu-id="3a83c-103">Löscht die angegebene Azure Site Recovery Protection-Container Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="3a83c-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a83c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a83c-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a83c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a83c-105">DESCRIPTION</span></span>
<span data-ttu-id="3a83c-106">Das Cmdlet **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** löscht die angegebene Zuordnung des angegebenen Azure Site Recovery Protection-Containers.</span><span class="sxs-lookup"><span data-stu-id="3a83c-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="3a83c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a83c-107">EXAMPLES</span></span>

### <span data-ttu-id="3a83c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3a83c-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="3a83c-109">Startet das Löschen der angegebenen Schutzcontainer Zuordnung und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a83c-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3a83c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a83c-110">PARAMETERS</span></span>

### <span data-ttu-id="3a83c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3a83c-111">-Force</span></span>
<span data-ttu-id="3a83c-112">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3a83c-112">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a83c-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3a83c-113">-InputObject</span></span>
<span data-ttu-id="3a83c-114">Das Eingabeobjekt für das Cmdlet: das Container Zuordnungsobjekt für ASR-Schutz, das dem zu löschenden Schutzcontainer entspricht.</span><span class="sxs-lookup"><span data-stu-id="3a83c-114">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a83c-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a83c-115">-Confirm</span></span>
<span data-ttu-id="3a83c-116">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3a83c-116">Specify if confirmation is required.</span></span> <span data-ttu-id="3a83c-117">Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="3a83c-117">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="3a83c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a83c-118">-WhatIf</span></span>
<span data-ttu-id="3a83c-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3a83c-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="3a83c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a83c-120">CommonParameters</span></span>
<span data-ttu-id="3a83c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a83c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a83c-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a83c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a83c-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a83c-123">INPUTS</span></span>

### <span data-ttu-id="3a83c-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3a83c-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="3a83c-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a83c-125">OUTPUTS</span></span>

### <span data-ttu-id="3a83c-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3a83c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3a83c-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a83c-127">NOTES</span></span>

## <span data-ttu-id="3a83c-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a83c-128">RELATED LINKS</span></span>

[<span data-ttu-id="3a83c-129">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3a83c-129">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="3a83c-130">Neu – AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3a83c-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
