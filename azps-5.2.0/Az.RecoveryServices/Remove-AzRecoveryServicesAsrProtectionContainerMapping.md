---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 25475bd87579b693555280f3c465f157d69c807a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308224"
---
# <span data-ttu-id="ffc39-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ffc39-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="ffc39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffc39-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc39-103">Löscht die angegebene Azure Site Recovery Protection-Containerzuordnung.</span><span class="sxs-lookup"><span data-stu-id="ffc39-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="ffc39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffc39-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc39-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffc39-105">DESCRIPTION</span></span>
<span data-ttu-id="ffc39-106">Das **Cmdlet "Remove-AzRecoveryServicesAsrProtectionContainerMapping"** löscht die angegebene Azure Site Recovery Protection-Containerzuordnung.</span><span class="sxs-lookup"><span data-stu-id="ffc39-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="ffc39-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ffc39-107">EXAMPLES</span></span>

### <span data-ttu-id="ffc39-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ffc39-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="ffc39-109">Startet das Löschen der angegebenen Schutzcontainerzuordnung und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="ffc39-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ffc39-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffc39-110">PARAMETERS</span></span>

### <span data-ttu-id="ffc39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc39-111">-DefaultProfile</span></span>
<span data-ttu-id="ffc39-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ffc39-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ffc39-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ffc39-113">-Force</span></span>
<span data-ttu-id="ffc39-114">Erzwingen Sie die Ausführung des Befehls, ohne eine zusätzliche Warnung bereitstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="ffc39-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="ffc39-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffc39-115">-InputObject</span></span>
<span data-ttu-id="ffc39-116">Das Eingabeobjekt für das Cmdlet: das ASR-Schutzcontainerzuordnungsobjekt, das dem zu löschende Schutzcontainer entspricht.</span><span class="sxs-lookup"><span data-stu-id="ffc39-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="ffc39-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffc39-117">-Confirm</span></span>
<span data-ttu-id="ffc39-118">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ffc39-118">Specify if confirmation is required.</span></span> <span data-ttu-id="ffc39-119">Legen Sie den Wert des Bestätigungsparameters auf "$false, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="ffc39-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="ffc39-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ffc39-120">-WhatIf</span></span>
<span data-ttu-id="ffc39-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ffc39-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="ffc39-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc39-122">CommonParameters</span></span>
<span data-ttu-id="ffc39-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffc39-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc39-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffc39-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc39-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ffc39-125">INPUTS</span></span>

### <span data-ttu-id="ffc39-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ffc39-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="ffc39-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ffc39-127">OUTPUTS</span></span>

### <span data-ttu-id="ffc39-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ffc39-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ffc39-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ffc39-129">NOTES</span></span>

## <span data-ttu-id="ffc39-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ffc39-130">RELATED LINKS</span></span>

[<span data-ttu-id="ffc39-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ffc39-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="ffc39-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ffc39-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
