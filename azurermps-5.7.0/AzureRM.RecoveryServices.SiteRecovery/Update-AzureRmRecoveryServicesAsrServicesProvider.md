---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 823ad4b0f7eff8f80fea012bdef4b3c2662d55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478282"
---
# <span data-ttu-id="0a1b3-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0a1b3-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="0a1b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="0a1b3-103">Aktualisiert (Server aktualisieren) die Informationen, die vom Azure Site Recovery Services-Anbieter empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a1b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a1b3-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a1b3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a1b3-105">DESCRIPTION</span></span>
<span data-ttu-id="0a1b3-106">Mit dem Cmdlet **Update-AzureRmRecoveryServicesAsrServicesProvider** werden die vom Azure Site Recovery Services-Anbieter empfangenen Informationen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="0a1b3-107">Mit diesem Cmdlet können Sie eine Aktualisierung der vom Wiederherstellungsdienste-Anbieter empfangenen Informationen auslösen.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="0a1b3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a1b3-108">EXAMPLES</span></span>

### <span data-ttu-id="0a1b3-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a1b3-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="0a1b3-110">Startet den Vorgang zum Aktualisieren der Informationen vom angegebenen ASR-Dienstanbieter und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0a1b3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a1b3-111">PARAMETERS</span></span>

### <span data-ttu-id="0a1b3-112">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0a1b3-112">-Confirm</span></span>
<span data-ttu-id="0a1b3-113">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a1b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a1b3-114">-DefaultProfile</span></span>
<span data-ttu-id="0a1b3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a1b3-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0a1b3-116">-InputObject</span></span>
<span data-ttu-id="0a1b3-117">Gibt das Dienstanbieterobjekt für ASR-Dienste an, das den Server identifiziert, für den Informationen aktualisiert werden sollen (aktualisiert).</span><span class="sxs-lookup"><span data-stu-id="0a1b3-117">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a1b3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a1b3-118">-WhatIf</span></span>
<span data-ttu-id="0a1b3-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a1b3-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a1b3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a1b3-121">CommonParameters</span></span>
<span data-ttu-id="0a1b3-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a1b3-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a1b3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a1b3-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a1b3-124">INPUTS</span></span>

### <span data-ttu-id="0a1b3-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0a1b3-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="0a1b3-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a1b3-126">OUTPUTS</span></span>

### <span data-ttu-id="0a1b3-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="0a1b3-127">System.Object</span></span>

## <span data-ttu-id="0a1b3-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a1b3-128">NOTES</span></span>

## <span data-ttu-id="0a1b3-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a1b3-129">RELATED LINKS</span></span>

[<span data-ttu-id="0a1b3-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0a1b3-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="0a1b3-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0a1b3-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
