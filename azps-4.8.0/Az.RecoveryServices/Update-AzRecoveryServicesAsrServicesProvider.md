---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174446"
---
# <span data-ttu-id="1840f-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1840f-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="1840f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1840f-102">SYNOPSIS</span></span>
<span data-ttu-id="1840f-103">Aktualisiert (Server aktualisieren) die Informationen, die vom Azure Site Recovery Services-Anbieter empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="1840f-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="1840f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1840f-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1840f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1840f-105">DESCRIPTION</span></span>
<span data-ttu-id="1840f-106">Mit dem Cmdlet **Update-AzRecoveryServicesAsrServicesProvider** werden die vom Azure Site Recovery Services-Anbieter empfangenen Informationen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1840f-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="1840f-107">Mit diesem Cmdlet können Sie eine Aktualisierung der vom Wiederherstellungsdienste-Anbieter empfangenen Informationen auslösen.</span><span class="sxs-lookup"><span data-stu-id="1840f-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="1840f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1840f-108">EXAMPLES</span></span>

### <span data-ttu-id="1840f-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1840f-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="1840f-110">Startet den Vorgang zum Aktualisieren der Informationen vom angegebenen ASR-Dienstanbieter und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1840f-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1840f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1840f-111">PARAMETERS</span></span>

### <span data-ttu-id="1840f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1840f-112">-DefaultProfile</span></span>
<span data-ttu-id="1840f-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1840f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1840f-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1840f-114">-InputObject</span></span>
<span data-ttu-id="1840f-115">Gibt das Dienstanbieterobjekt für ASR-Dienste an, das den Server identifiziert, für den Informationen aktualisiert werden sollen (aktualisiert).</span><span class="sxs-lookup"><span data-stu-id="1840f-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="1840f-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1840f-116">-Confirm</span></span>
<span data-ttu-id="1840f-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1840f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1840f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1840f-118">-WhatIf</span></span>
<span data-ttu-id="1840f-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1840f-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1840f-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1840f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1840f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1840f-121">CommonParameters</span></span>
<span data-ttu-id="1840f-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1840f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1840f-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1840f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1840f-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1840f-124">INPUTS</span></span>

### <span data-ttu-id="1840f-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1840f-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="1840f-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1840f-126">OUTPUTS</span></span>

### <span data-ttu-id="1840f-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1840f-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1840f-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="1840f-128">NOTES</span></span>

## <span data-ttu-id="1840f-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1840f-129">RELATED LINKS</span></span>

[<span data-ttu-id="1840f-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1840f-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="1840f-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1840f-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
