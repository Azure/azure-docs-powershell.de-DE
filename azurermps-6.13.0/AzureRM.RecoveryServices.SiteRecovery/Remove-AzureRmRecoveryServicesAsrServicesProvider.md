---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 4de1861c3db804e7ffd4371f4e35c241843374cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477790"
---
# <span data-ttu-id="24b79-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="24b79-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="24b79-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24b79-102">SYNOPSIS</span></span>
<span data-ttu-id="24b79-103">Löscht/hebt die Registrierung des angegebenen Azure Site Recovery Recovery Services-Anbieters aus dem Vault für Wiederherstellungsdienste auf.</span><span class="sxs-lookup"><span data-stu-id="24b79-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24b79-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24b79-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24b79-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24b79-105">DESCRIPTION</span></span>
<span data-ttu-id="24b79-106">Mit dem Cmdlet **Remove-AzureRmRecoveryServicesAsrServicesProvider** wird der angegebene Azure Site Recovery Recovery Services-Anbieter aus dem Tresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="24b79-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="24b79-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24b79-107">EXAMPLES</span></span>

### <span data-ttu-id="24b79-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="24b79-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="24b79-109">Startet die Löschung/Aufhebung der Registrierung des angegebenen Azure Site Recovery Services-Anbieters und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="24b79-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="24b79-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="24b79-110">PARAMETERS</span></span>

### <span data-ttu-id="24b79-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b79-111">-DefaultProfile</span></span>
<span data-ttu-id="24b79-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24b79-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b79-113">-Force</span><span class="sxs-lookup"><span data-stu-id="24b79-113">-Force</span></span>
<span data-ttu-id="24b79-114">Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="24b79-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="24b79-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="24b79-115">-InputObject</span></span>
<span data-ttu-id="24b79-116">Das Eingabeobjekt für das Cmdlet: das Dienstanbieterobjekt für ASR-Wiederherstellungsdienste, das dem zu löschenden Dienstanbieter für ASR-Wiederherstellungsdienste entspricht.</span><span class="sxs-lookup"><span data-stu-id="24b79-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="24b79-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="24b79-117">-Confirm</span></span>
<span data-ttu-id="24b79-118">Geben Sie an, ob eine Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="24b79-118">Specify if confirmation is required.</span></span> <span data-ttu-id="24b79-119">Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="24b79-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="24b79-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24b79-120">-WhatIf</span></span>
<span data-ttu-id="24b79-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="24b79-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="24b79-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b79-122">CommonParameters</span></span>
<span data-ttu-id="24b79-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24b79-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b79-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24b79-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b79-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24b79-125">INPUTS</span></span>

### <span data-ttu-id="24b79-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="24b79-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="24b79-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24b79-127">OUTPUTS</span></span>

### <span data-ttu-id="24b79-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="24b79-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="24b79-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="24b79-129">NOTES</span></span>

## <span data-ttu-id="24b79-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24b79-130">RELATED LINKS</span></span>

[<span data-ttu-id="24b79-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="24b79-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="24b79-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="24b79-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
