---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: dcc0424cd1d6dbd823793a3dc77e813c6e182176
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664524"
---
# <span data-ttu-id="1857d-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="1857d-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="1857d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1857d-102">SYNOPSIS</span></span>
<span data-ttu-id="1857d-103">Löscht die angegebene ASR-Replikationsrichtlinie aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="1857d-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1857d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1857d-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1857d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1857d-105">DESCRIPTION</span></span>
<span data-ttu-id="1857d-106">Das Cmdlet " **Remove-AzureRmRecoveryServicesAsrPolicy** " hat die angegebene Replikationsrichtlinie aus dem Vault für Wiederherstellungsdienste gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1857d-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="1857d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1857d-107">EXAMPLES</span></span>

### <span data-ttu-id="1857d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1857d-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="1857d-109">Startet das Löschen der angegebenen Replikationsrichtlinie und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1857d-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1857d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1857d-110">PARAMETERS</span></span>

### <span data-ttu-id="1857d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1857d-111">-DefaultProfile</span></span>
<span data-ttu-id="1857d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1857d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1857d-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1857d-113">-InputObject</span></span>
<span data-ttu-id="1857d-114">Das Eingabeobjekt für das Cmdlet: das ASR-Replikationsrichtlinien Objekt, das der zu löschenden Replikationsrichtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="1857d-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1857d-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1857d-115">-Confirm</span></span>
<span data-ttu-id="1857d-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1857d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1857d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1857d-117">-WhatIf</span></span>
<span data-ttu-id="1857d-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1857d-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1857d-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1857d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1857d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1857d-120">CommonParameters</span></span>
<span data-ttu-id="1857d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1857d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1857d-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1857d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1857d-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1857d-123">INPUTS</span></span>

### <span data-ttu-id="1857d-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="1857d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="1857d-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1857d-125">OUTPUTS</span></span>

### <span data-ttu-id="1857d-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="1857d-126">System.Object</span></span>

## <span data-ttu-id="1857d-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="1857d-127">NOTES</span></span>

## <span data-ttu-id="1857d-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1857d-128">RELATED LINKS</span></span>

[<span data-ttu-id="1857d-129">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="1857d-129">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="1857d-130">Neu – AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="1857d-130">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
