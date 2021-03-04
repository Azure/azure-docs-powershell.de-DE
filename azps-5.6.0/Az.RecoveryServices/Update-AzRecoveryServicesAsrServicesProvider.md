---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 83dbf747e2ddcd001320ac746b7c505df73a8169
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927635"
---
# <span data-ttu-id="8a24b-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8a24b-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="8a24b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a24b-102">SYNOPSIS</span></span>
<span data-ttu-id="8a24b-103">Aktualisiert (Aktualisierungsserver) die Vom Azure Site Recovery Services Provider empfangenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="8a24b-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="8a24b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a24b-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a24b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a24b-105">DESCRIPTION</span></span>
<span data-ttu-id="8a24b-106">Das **Cmdlet Update-AzRecoveryServicesAsrServicesProvider** aktualisiert die vom Azure Site Recovery Services Provider empfangenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="8a24b-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="8a24b-107">Sie können dieses Cmdlet verwenden, um eine Aktualisierung der vom Wiederherstellungsdiensteanbieter empfangenen Informationen auszulösen.</span><span class="sxs-lookup"><span data-stu-id="8a24b-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="8a24b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a24b-108">EXAMPLES</span></span>

### <span data-ttu-id="8a24b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a24b-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="8a24b-110">Startet den Vorgang zum Aktualisieren der Informationen vom angegebenen ASR-Dienstanbieter und gibt den ZUM Nachverfolgen des Vorgangs verwendeten ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="8a24b-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8a24b-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8a24b-111">PARAMETERS</span></span>

### <span data-ttu-id="8a24b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a24b-112">-DefaultProfile</span></span>
<span data-ttu-id="8a24b-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a24b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8a24b-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a24b-114">-InputObject</span></span>
<span data-ttu-id="8a24b-115">Gibt das ASR-Anbieterobjekt an, das den Server angibt, für den Informationen aktualisiert(aktualisiert) werden.</span><span class="sxs-lookup"><span data-stu-id="8a24b-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="8a24b-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a24b-116">-Confirm</span></span>
<span data-ttu-id="8a24b-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a24b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a24b-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a24b-118">-WhatIf</span></span>
<span data-ttu-id="8a24b-119">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a24b-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a24b-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a24b-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a24b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a24b-121">CommonParameters</span></span>
<span data-ttu-id="8a24b-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a24b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a24b-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a24b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a24b-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a24b-124">INPUTS</span></span>

### <span data-ttu-id="8a24b-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8a24b-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="8a24b-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a24b-126">OUTPUTS</span></span>

### <span data-ttu-id="8a24b-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="8a24b-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8a24b-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8a24b-128">NOTES</span></span>

## <span data-ttu-id="8a24b-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8a24b-129">RELATED LINKS</span></span>

[<span data-ttu-id="8a24b-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8a24b-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="8a24b-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8a24b-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
