---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151073"
---
# <span data-ttu-id="c7071-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c7071-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="c7071-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7071-102">SYNOPSIS</span></span>
<span data-ttu-id="c7071-103">Aktualisiert (Aktualisierungsserver) die Vom Azure Site Recovery Services-Anbieter erhaltenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="c7071-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="c7071-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7071-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7071-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7071-105">DESCRIPTION</span></span>
<span data-ttu-id="c7071-106">Das **Cmdlet "Update-AzRecoveryServicesAsrServicesProvider"** aktualisiert die Vom Azure Site Recovery Services-Anbieter erhaltenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="c7071-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="c7071-107">Sie können dieses Cmdlet verwenden, um eine Aktualisierung der Vom Wiederherstellungsdiensteanbieter erhaltenen Informationen auszulösen.</span><span class="sxs-lookup"><span data-stu-id="c7071-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="c7071-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c7071-108">EXAMPLES</span></span>

### <span data-ttu-id="c7071-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c7071-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="c7071-110">Startet den Vorgang zum Aktualisieren der Informationen des angegebenen ASR-Dienstanbieters und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="c7071-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c7071-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7071-111">PARAMETERS</span></span>

### <span data-ttu-id="c7071-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7071-112">-DefaultProfile</span></span>
<span data-ttu-id="c7071-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7071-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c7071-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7071-114">-InputObject</span></span>
<span data-ttu-id="c7071-115">Gibt das ASR-Dienstanbieterobjekt an, das den Server identifiziert, für den Die Informationen aktualisiert (aktualisiert) werden.</span><span class="sxs-lookup"><span data-stu-id="c7071-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="c7071-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7071-116">-Confirm</span></span>
<span data-ttu-id="c7071-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7071-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7071-118">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c7071-118">-WhatIf</span></span>
<span data-ttu-id="c7071-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7071-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7071-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7071-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7071-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7071-121">CommonParameters</span></span>
<span data-ttu-id="c7071-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7071-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7071-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7071-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7071-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c7071-124">INPUTS</span></span>

### <span data-ttu-id="c7071-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c7071-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="c7071-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c7071-126">OUTPUTS</span></span>

### <span data-ttu-id="c7071-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c7071-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c7071-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c7071-128">NOTES</span></span>

## <span data-ttu-id="c7071-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c7071-129">RELATED LINKS</span></span>

[<span data-ttu-id="c7071-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c7071-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="c7071-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c7071-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
