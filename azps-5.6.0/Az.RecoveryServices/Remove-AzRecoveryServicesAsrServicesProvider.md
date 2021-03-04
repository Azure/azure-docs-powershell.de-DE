---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: f3c18813cd3c002270d655b88fbc9285338a4338
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919187"
---
# <span data-ttu-id="f7c26-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f7c26-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="f7c26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7c26-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c26-103">Löscht/entregistert den angegebenen Azure Websitewiederherstellungsdienstanbieter aus dem Wiederherstellungsdienste-Tresor.</span><span class="sxs-lookup"><span data-stu-id="f7c26-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="f7c26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7c26-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7c26-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7c26-105">DESCRIPTION</span></span>
<span data-ttu-id="f7c26-106">Das **Cmdlet Remove-AzRecoveryServicesAsrServicesProvider** entfernt den angegebenen Azure Site Recovery Services-Anbieter aus dem Tresor.</span><span class="sxs-lookup"><span data-stu-id="f7c26-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="f7c26-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7c26-107">EXAMPLES</span></span>

### <span data-ttu-id="f7c26-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7c26-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="f7c26-109">Startet das Löschen/Abmelden des angegebenen Azure Site Recovery-Dienstanbieters und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f7c26-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f7c26-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f7c26-110">PARAMETERS</span></span>

### <span data-ttu-id="f7c26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c26-111">-DefaultProfile</span></span>
<span data-ttu-id="f7c26-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7c26-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f7c26-113">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="f7c26-113">-Force</span></span>
<span data-ttu-id="f7c26-114">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne eine zusätzliche Warnung zu geben.</span><span class="sxs-lookup"><span data-stu-id="f7c26-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="f7c26-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7c26-115">-InputObject</span></span>
<span data-ttu-id="f7c26-116">Das Eingabeobjekt für das Cmdlet: Das ASR-Wiederherstellungsdienstanbieterobjekt, das dem zu löschende ASR-Wiederherstellungsdienstanbieter entspricht.</span><span class="sxs-lookup"><span data-stu-id="f7c26-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="f7c26-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7c26-117">-Confirm</span></span>
<span data-ttu-id="f7c26-118">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f7c26-118">Specify if confirmation is required.</span></span> <span data-ttu-id="f7c26-119">Legen Sie den Wert des Bestätigungsparameters auf $false, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="f7c26-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="f7c26-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7c26-120">-WhatIf</span></span>
<span data-ttu-id="f7c26-121">Zeigt, was geschehen würde, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f7c26-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="f7c26-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c26-122">CommonParameters</span></span>
<span data-ttu-id="f7c26-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7c26-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c26-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7c26-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c26-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7c26-125">INPUTS</span></span>

### <span data-ttu-id="f7c26-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f7c26-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="f7c26-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7c26-127">OUTPUTS</span></span>

### <span data-ttu-id="f7c26-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="f7c26-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f7c26-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f7c26-129">NOTES</span></span>

## <span data-ttu-id="f7c26-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f7c26-130">RELATED LINKS</span></span>

[<span data-ttu-id="f7c26-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f7c26-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="f7c26-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f7c26-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
