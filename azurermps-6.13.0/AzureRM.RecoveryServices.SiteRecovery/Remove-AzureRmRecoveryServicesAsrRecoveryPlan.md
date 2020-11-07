---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b3bedc5c521736ff702f5e7378b4c401a42bce5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662310"
---
# <span data-ttu-id="9fe31-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9fe31-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="9fe31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9fe31-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe31-103">Löscht den angegebenen ASR-Wiederherstellungsplan aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="9fe31-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fe31-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fe31-104">SYNTAX</span></span>

### <span data-ttu-id="9fe31-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="9fe31-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe31-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9fe31-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe31-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fe31-107">DESCRIPTION</span></span>
<span data-ttu-id="9fe31-108">Das Cmdlet **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** löscht den angegebenen Wiederherstellungsplan aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="9fe31-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="9fe31-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fe31-109">EXAMPLES</span></span>

### <span data-ttu-id="9fe31-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9fe31-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="9fe31-111">Startet den Löschvorgang des angegebenen Wiederherstellungsplans und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9fe31-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9fe31-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fe31-112">PARAMETERS</span></span>

### <span data-ttu-id="9fe31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe31-113">-DefaultProfile</span></span>
<span data-ttu-id="9fe31-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9fe31-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9fe31-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9fe31-115">-InputObject</span></span>
<span data-ttu-id="9fe31-116">Das Eingabeobjekt für das Cmdlet: das ASR-Wiederherstellungsplan Objekt, das dem Wiederherstellungsplan entspricht, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="9fe31-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe31-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9fe31-117">-Name</span></span>
<span data-ttu-id="9fe31-118">Gibt den Namen des Wiederherstellungsplans an, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="9fe31-118">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe31-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9fe31-119">-Confirm</span></span>
<span data-ttu-id="9fe31-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9fe31-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe31-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe31-121">-WhatIf</span></span>
<span data-ttu-id="9fe31-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fe31-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fe31-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9fe31-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe31-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe31-124">CommonParameters</span></span>
<span data-ttu-id="9fe31-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fe31-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe31-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe31-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe31-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9fe31-127">INPUTS</span></span>

### <span data-ttu-id="9fe31-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9fe31-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="9fe31-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9fe31-129">OUTPUTS</span></span>

### <span data-ttu-id="9fe31-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="9fe31-130">System.Object</span></span>

## <span data-ttu-id="9fe31-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="9fe31-131">NOTES</span></span>

## <span data-ttu-id="9fe31-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9fe31-132">RELATED LINKS</span></span>

[<span data-ttu-id="9fe31-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9fe31-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9fe31-134">Neu – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9fe31-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9fe31-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9fe31-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


