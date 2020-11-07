---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 9a67729b384703ccc102b14d521d4422825bdb6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659850"
---
# <span data-ttu-id="53c74-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="53c74-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="53c74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53c74-102">SYNOPSIS</span></span>
<span data-ttu-id="53c74-103">Löscht den angegebenen Azure Site Recovery-Stoff aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="53c74-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="53c74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53c74-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53c74-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53c74-105">DESCRIPTION</span></span>
<span data-ttu-id="53c74-106">Das Cmdlet " **Remove-AzRecoveryServicesAsrFabric** " entfernt das angegebene Azure Site Recovery-Fabric aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="53c74-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="53c74-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53c74-107">EXAMPLES</span></span>

### <span data-ttu-id="53c74-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53c74-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="53c74-109">Startet das Löschen des angegebenen Fabrics und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="53c74-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="53c74-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="53c74-110">PARAMETERS</span></span>

### <span data-ttu-id="53c74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c74-111">-DefaultProfile</span></span>
<span data-ttu-id="53c74-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53c74-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="53c74-113">-Force</span><span class="sxs-lookup"><span data-stu-id="53c74-113">-Force</span></span>
<span data-ttu-id="53c74-114">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="53c74-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="53c74-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="53c74-115">-InputObject</span></span>
<span data-ttu-id="53c74-116">Das Eingabeobjekt für das Cmdlet: das ASR-Fabric-Objekt, das dem zu löschenden Stoff entspricht.</span><span class="sxs-lookup"><span data-stu-id="53c74-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="53c74-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="53c74-117">-Confirm</span></span>
<span data-ttu-id="53c74-118">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="53c74-118">Specify if confirmation is required.</span></span> <span data-ttu-id="53c74-119">Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="53c74-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="53c74-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c74-120">-WhatIf</span></span>
<span data-ttu-id="53c74-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="53c74-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="53c74-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c74-122">CommonParameters</span></span>
<span data-ttu-id="53c74-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c74-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c74-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53c74-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c74-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53c74-125">INPUTS</span></span>

### <span data-ttu-id="53c74-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="53c74-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="53c74-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53c74-127">OUTPUTS</span></span>

### <span data-ttu-id="53c74-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="53c74-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="53c74-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="53c74-129">NOTES</span></span>

## <span data-ttu-id="53c74-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53c74-130">RELATED LINKS</span></span>

[<span data-ttu-id="53c74-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="53c74-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="53c74-132">Neu – AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="53c74-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
