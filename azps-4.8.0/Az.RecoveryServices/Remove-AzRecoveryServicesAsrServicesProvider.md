---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9a9fbf8c25eba6206b3852476b5a72a2f96be423
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167417"
---
# <span data-ttu-id="3deb8-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3deb8-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="3deb8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3deb8-102">SYNOPSIS</span></span>
<span data-ttu-id="3deb8-103">Löscht/hebt die Registrierung des angegebenen Azure Site Recovery Recovery Services-Anbieters aus dem Vault für Wiederherstellungsdienste auf.</span><span class="sxs-lookup"><span data-stu-id="3deb8-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="3deb8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3deb8-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3deb8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3deb8-105">DESCRIPTION</span></span>
<span data-ttu-id="3deb8-106">Mit dem Cmdlet **Remove-AzRecoveryServicesAsrServicesProvider** wird der angegebene Azure Site Recovery Recovery Services-Anbieter aus dem Tresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="3deb8-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="3deb8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3deb8-107">EXAMPLES</span></span>

### <span data-ttu-id="3deb8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3deb8-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="3deb8-109">Startet die Löschung/Aufhebung der Registrierung des angegebenen Azure Site Recovery Services-Anbieters und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3deb8-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3deb8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3deb8-110">PARAMETERS</span></span>

### <span data-ttu-id="3deb8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3deb8-111">-DefaultProfile</span></span>
<span data-ttu-id="3deb8-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3deb8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3deb8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3deb8-113">-Force</span></span>
<span data-ttu-id="3deb8-114">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3deb8-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="3deb8-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3deb8-115">-InputObject</span></span>
<span data-ttu-id="3deb8-116">Das Eingabeobjekt für das Cmdlet: das Dienstanbieterobjekt für ASR-Wiederherstellungsdienste, das dem zu löschenden Dienstanbieter für ASR-Wiederherstellungsdienste entspricht.</span><span class="sxs-lookup"><span data-stu-id="3deb8-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3deb8-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3deb8-117">-Confirm</span></span>
<span data-ttu-id="3deb8-118">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3deb8-118">Specify if confirmation is required.</span></span> <span data-ttu-id="3deb8-119">Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="3deb8-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="3deb8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3deb8-120">-WhatIf</span></span>
<span data-ttu-id="3deb8-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3deb8-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="3deb8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3deb8-122">CommonParameters</span></span>
<span data-ttu-id="3deb8-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3deb8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3deb8-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3deb8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3deb8-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3deb8-125">INPUTS</span></span>

### <span data-ttu-id="3deb8-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3deb8-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="3deb8-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3deb8-127">OUTPUTS</span></span>

### <span data-ttu-id="3deb8-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3deb8-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3deb8-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="3deb8-129">NOTES</span></span>

## <span data-ttu-id="3deb8-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3deb8-130">RELATED LINKS</span></span>

[<span data-ttu-id="3deb8-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3deb8-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="3deb8-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3deb8-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
