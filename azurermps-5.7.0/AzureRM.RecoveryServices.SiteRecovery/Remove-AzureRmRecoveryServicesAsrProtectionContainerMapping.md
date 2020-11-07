---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 7a2508669c0beba7fc9edd92ac645ce149633e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663052"
---
# <span data-ttu-id="09fb2-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="09fb2-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="09fb2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="09fb2-103">Löscht die angegebene Azure Site Recovery Protection-Container Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="09fb2-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09fb2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09fb2-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09fb2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09fb2-105">DESCRIPTION</span></span>
<span data-ttu-id="09fb2-106">Das Cmdlet **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** löscht die angegebene Zuordnung des angegebenen Azure Site Recovery Protection-Containers.</span><span class="sxs-lookup"><span data-stu-id="09fb2-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="09fb2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09fb2-107">EXAMPLES</span></span>

### <span data-ttu-id="09fb2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="09fb2-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="09fb2-109">Startet das Löschen der angegebenen Schutzcontainer Zuordnung und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="09fb2-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="09fb2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="09fb2-110">PARAMETERS</span></span>

### <span data-ttu-id="09fb2-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="09fb2-111">-Confirm</span></span>
<span data-ttu-id="09fb2-112">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="09fb2-112">Specify if confirmation is required.</span></span> <span data-ttu-id="09fb2-113">Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="09fb2-113">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="09fb2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fb2-114">-DefaultProfile</span></span>
<span data-ttu-id="09fb2-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09fb2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="09fb2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="09fb2-116">-Force</span></span>
<span data-ttu-id="09fb2-117">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="09fb2-117">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="09fb2-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="09fb2-118">-InputObject</span></span>
<span data-ttu-id="09fb2-119">Das Eingabeobjekt für das Cmdlet: das Container Zuordnungsobjekt für ASR-Schutz, das dem zu löschenden Schutzcontainer entspricht.</span><span class="sxs-lookup"><span data-stu-id="09fb2-119">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="09fb2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09fb2-120">-WhatIf</span></span>
<span data-ttu-id="09fb2-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="09fb2-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="09fb2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fb2-122">CommonParameters</span></span>
<span data-ttu-id="09fb2-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09fb2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fb2-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09fb2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fb2-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09fb2-125">INPUTS</span></span>

### <span data-ttu-id="09fb2-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="09fb2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="09fb2-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09fb2-127">OUTPUTS</span></span>

### <span data-ttu-id="09fb2-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="09fb2-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="09fb2-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="09fb2-129">NOTES</span></span>

## <span data-ttu-id="09fb2-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09fb2-130">RELATED LINKS</span></span>

[<span data-ttu-id="09fb2-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="09fb2-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="09fb2-132">Neu – AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="09fb2-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
