---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 095759ca2753cac4f7155430a241e0554e910fd6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308248"
---
# <span data-ttu-id="221db-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="221db-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="221db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="221db-102">SYNOPSIS</span></span>
<span data-ttu-id="221db-103">Löscht das angegebene Azure Site Recovery Fabric aus dem Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="221db-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="221db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="221db-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="221db-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="221db-105">DESCRIPTION</span></span>
<span data-ttu-id="221db-106">Das **Cmdlet "Remove-AzRecoveryServicesAsrFabric"** entfernt das angegebene Azure Site Recovery-Fabric aus dem Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="221db-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="221db-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="221db-107">EXAMPLES</span></span>

### <span data-ttu-id="221db-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="221db-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="221db-109">Startet das Löschen des angegebenen Fabric und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="221db-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="221db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="221db-110">PARAMETERS</span></span>

### <span data-ttu-id="221db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="221db-111">-DefaultProfile</span></span>
<span data-ttu-id="221db-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="221db-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="221db-113">-Force</span><span class="sxs-lookup"><span data-stu-id="221db-113">-Force</span></span>
<span data-ttu-id="221db-114">Erzwingen Sie die Ausführung des Befehls, ohne eine zusätzliche Warnung bereitstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="221db-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="221db-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="221db-115">-InputObject</span></span>
<span data-ttu-id="221db-116">Das Eingabeobjekt für das Cmdlet: Das ASR-Fabric-Objekt, das dem zu löschende Fabric entspricht.</span><span class="sxs-lookup"><span data-stu-id="221db-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="221db-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="221db-117">-Confirm</span></span>
<span data-ttu-id="221db-118">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="221db-118">Specify if confirmation is required.</span></span> <span data-ttu-id="221db-119">Legen Sie den Wert des Bestätigungsparameters auf "$false, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="221db-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="221db-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="221db-120">-WhatIf</span></span>
<span data-ttu-id="221db-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="221db-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="221db-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="221db-122">CommonParameters</span></span>
<span data-ttu-id="221db-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="221db-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="221db-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="221db-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="221db-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="221db-125">INPUTS</span></span>

### <span data-ttu-id="221db-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="221db-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="221db-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="221db-127">OUTPUTS</span></span>

### <span data-ttu-id="221db-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="221db-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="221db-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="221db-129">NOTES</span></span>

## <span data-ttu-id="221db-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="221db-130">RELATED LINKS</span></span>

[<span data-ttu-id="221db-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="221db-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="221db-132">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="221db-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
