---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: bb80bebc8c1a5dccbeedf4abd277891c3b2e9de7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919256"
---
# <span data-ttu-id="6dbe8-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6dbe8-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="6dbe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dbe8-102">SYNOPSIS</span></span>
<span data-ttu-id="6dbe8-103">Löscht die angegebene ASR-Netzwerkzuordnung aus dem Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="6dbe8-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="6dbe8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6dbe8-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dbe8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6dbe8-105">DESCRIPTION</span></span>
<span data-ttu-id="6dbe8-106">Das **Cmdlet Remove-AzRecoveryServicesAsrNetworkMapping** löscht die angegebene ASR-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="6dbe8-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="6dbe8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6dbe8-107">EXAMPLES</span></span>

### <span data-ttu-id="6dbe8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6dbe8-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="6dbe8-109">Startet das Löschen der angegebenen ASR-Netzwerkzuordnung und gibt den ZUM Nachverfolgen des Vorgangs verwendeten ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="6dbe8-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6dbe8-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6dbe8-110">PARAMETERS</span></span>

### <span data-ttu-id="6dbe8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dbe8-111">-DefaultProfile</span></span>
<span data-ttu-id="6dbe8-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6dbe8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6dbe8-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dbe8-113">-InputObject</span></span>
<span data-ttu-id="6dbe8-114">Das Eingabeobjekt für das Cmdlet: Das ASR-Netzwerkzuordnungsobjekt, das der zu löschende ASR-Netzwerkzuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="6dbe8-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dbe8-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6dbe8-115">-Confirm</span></span>
<span data-ttu-id="6dbe8-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6dbe8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dbe8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dbe8-117">-WhatIf</span></span>
<span data-ttu-id="6dbe8-118">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6dbe8-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6dbe8-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6dbe8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dbe8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dbe8-120">CommonParameters</span></span>
<span data-ttu-id="6dbe8-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dbe8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dbe8-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dbe8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dbe8-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6dbe8-123">INPUTS</span></span>

### <span data-ttu-id="6dbe8-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6dbe8-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="6dbe8-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6dbe8-125">OUTPUTS</span></span>

### <span data-ttu-id="6dbe8-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6dbe8-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6dbe8-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6dbe8-127">NOTES</span></span>

## <span data-ttu-id="6dbe8-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6dbe8-128">RELATED LINKS</span></span>

[<span data-ttu-id="6dbe8-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6dbe8-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="6dbe8-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6dbe8-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
