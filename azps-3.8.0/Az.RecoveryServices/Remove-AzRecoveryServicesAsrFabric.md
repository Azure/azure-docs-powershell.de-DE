---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 095759ca2753cac4f7155430a241e0554e910fd6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997345"
---
# <span data-ttu-id="75fb1-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="75fb1-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="75fb1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="75fb1-103">Löscht den angegebenen Azure Site Recovery-Stoff aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="75fb1-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="75fb1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75fb1-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75fb1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="75fb1-106">Das Cmdlet " **Remove-AzRecoveryServicesAsrFabric** " entfernt das angegebene Azure Site Recovery-Fabric aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="75fb1-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="75fb1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75fb1-107">EXAMPLES</span></span>

### <span data-ttu-id="75fb1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75fb1-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="75fb1-109">Startet das Löschen des angegebenen Fabrics und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="75fb1-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="75fb1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="75fb1-110">PARAMETERS</span></span>

### <span data-ttu-id="75fb1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75fb1-111">-DefaultProfile</span></span>
<span data-ttu-id="75fb1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75fb1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="75fb1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="75fb1-113">-Force</span></span>
<span data-ttu-id="75fb1-114">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="75fb1-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="75fb1-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="75fb1-115">-InputObject</span></span>
<span data-ttu-id="75fb1-116">Das Eingabeobjekt für das Cmdlet: das ASR-Fabric-Objekt, das dem zu löschenden Stoff entspricht.</span><span class="sxs-lookup"><span data-stu-id="75fb1-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="75fb1-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75fb1-117">-Confirm</span></span>
<span data-ttu-id="75fb1-118">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="75fb1-118">Specify if confirmation is required.</span></span> <span data-ttu-id="75fb1-119">Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="75fb1-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="75fb1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75fb1-120">-WhatIf</span></span>
<span data-ttu-id="75fb1-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="75fb1-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="75fb1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75fb1-122">CommonParameters</span></span>
<span data-ttu-id="75fb1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75fb1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75fb1-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75fb1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75fb1-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75fb1-125">INPUTS</span></span>

### <span data-ttu-id="75fb1-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="75fb1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="75fb1-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75fb1-127">OUTPUTS</span></span>

### <span data-ttu-id="75fb1-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="75fb1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="75fb1-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="75fb1-129">NOTES</span></span>

## <span data-ttu-id="75fb1-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75fb1-130">RELATED LINKS</span></span>

[<span data-ttu-id="75fb1-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="75fb1-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="75fb1-132">Neu – AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="75fb1-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
