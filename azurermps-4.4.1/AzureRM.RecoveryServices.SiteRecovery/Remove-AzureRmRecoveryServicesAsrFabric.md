---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 3f380110359668af5c1b506e1736d3ecc9f39b3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481682"
---
# <span data-ttu-id="79049-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="79049-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="79049-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79049-102">SYNOPSIS</span></span>
<span data-ttu-id="79049-103">Löscht den angegebenen Azure Site Recovery-Stoff aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="79049-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79049-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79049-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79049-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79049-105">DESCRIPTION</span></span>
<span data-ttu-id="79049-106">Das Cmdlet " **Remove-AzureRmRecoveryServicesAsrFabric** " entfernt das angegebene Azure Site Recovery-Fabric aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="79049-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="79049-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79049-107">EXAMPLES</span></span>

### <span data-ttu-id="79049-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79049-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="79049-109">Startet das Löschen des angegebenen Fabrics und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="79049-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="79049-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="79049-110">PARAMETERS</span></span>

### <span data-ttu-id="79049-111">-Force</span><span class="sxs-lookup"><span data-stu-id="79049-111">-Force</span></span>
<span data-ttu-id="79049-112">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="79049-112">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="79049-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="79049-113">-InputObject</span></span>
<span data-ttu-id="79049-114">Das Eingabeobjekt für das Cmdlet: das ASR-Fabric-Objekt, das dem zu löschenden Stoff entspricht.</span><span class="sxs-lookup"><span data-stu-id="79049-114">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79049-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79049-115">-Confirm</span></span>
<span data-ttu-id="79049-116">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="79049-116">Specify if confirmation is required.</span></span> <span data-ttu-id="79049-117">Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="79049-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="79049-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79049-118">-WhatIf</span></span>
<span data-ttu-id="79049-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="79049-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="79049-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79049-120">CommonParameters</span></span>
<span data-ttu-id="79049-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79049-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79049-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79049-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79049-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79049-123">INPUTS</span></span>

### <span data-ttu-id="79049-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="79049-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="79049-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79049-125">OUTPUTS</span></span>

### <span data-ttu-id="79049-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="79049-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="79049-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="79049-127">NOTES</span></span>

## <span data-ttu-id="79049-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79049-128">RELATED LINKS</span></span>

[<span data-ttu-id="79049-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="79049-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="79049-130">Neu – AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="79049-130">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
