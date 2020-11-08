---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 25475bd87579b693555280f3c465f157d69c807a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997339"
---
# <span data-ttu-id="33f6a-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="33f6a-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="33f6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="33f6a-103">Löscht die angegebene Azure Site Recovery Protection-Container Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="33f6a-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="33f6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33f6a-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33f6a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33f6a-105">DESCRIPTION</span></span>
<span data-ttu-id="33f6a-106">Das Cmdlet **Remove-AzRecoveryServicesAsrProtectionContainerMapping** löscht die angegebene Zuordnung des angegebenen Azure Site Recovery Protection-Containers.</span><span class="sxs-lookup"><span data-stu-id="33f6a-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="33f6a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33f6a-107">EXAMPLES</span></span>

### <span data-ttu-id="33f6a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="33f6a-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="33f6a-109">Startet das Löschen der angegebenen Schutzcontainer Zuordnung und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="33f6a-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="33f6a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="33f6a-110">PARAMETERS</span></span>

### <span data-ttu-id="33f6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33f6a-111">-DefaultProfile</span></span>
<span data-ttu-id="33f6a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33f6a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="33f6a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="33f6a-113">-Force</span></span>
<span data-ttu-id="33f6a-114">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="33f6a-114">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f6a-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="33f6a-115">-InputObject</span></span>
<span data-ttu-id="33f6a-116">Das Eingabeobjekt für das Cmdlet: das Container Zuordnungsobjekt für ASR-Schutz, das dem zu löschenden Schutzcontainer entspricht.</span><span class="sxs-lookup"><span data-stu-id="33f6a-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33f6a-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="33f6a-117">-Confirm</span></span>
<span data-ttu-id="33f6a-118">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="33f6a-118">Specify if confirmation is required.</span></span> <span data-ttu-id="33f6a-119">Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="33f6a-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="33f6a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33f6a-120">-WhatIf</span></span>
<span data-ttu-id="33f6a-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="33f6a-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="33f6a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f6a-122">CommonParameters</span></span>
<span data-ttu-id="33f6a-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33f6a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f6a-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33f6a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f6a-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33f6a-125">INPUTS</span></span>

### <span data-ttu-id="33f6a-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="33f6a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="33f6a-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33f6a-127">OUTPUTS</span></span>

### <span data-ttu-id="33f6a-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="33f6a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="33f6a-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="33f6a-129">NOTES</span></span>

## <span data-ttu-id="33f6a-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33f6a-130">RELATED LINKS</span></span>

[<span data-ttu-id="33f6a-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="33f6a-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="33f6a-132">Neu – AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="33f6a-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
