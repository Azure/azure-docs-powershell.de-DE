---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ef251bb9d1060e511658f9174cde2c04ab288ed7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308240"
---
# <span data-ttu-id="6391d-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6391d-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="6391d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6391d-102">SYNOPSIS</span></span>
<span data-ttu-id="6391d-103">Löscht die angegebene ASR-Netzwerkzuordnung aus dem Recovery Services-Tresor.</span><span class="sxs-lookup"><span data-stu-id="6391d-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="6391d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6391d-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6391d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6391d-105">DESCRIPTION</span></span>
<span data-ttu-id="6391d-106">Das **Cmdlet "Remove-AzRecoveryServicesAsrNetworkMapping"** löscht die angegebene ASR-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="6391d-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="6391d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6391d-107">EXAMPLES</span></span>

### <span data-ttu-id="6391d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6391d-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="6391d-109">Startet den Löschvorgang der angegebenen ASR-Netzwerkzuordnung und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="6391d-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6391d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6391d-110">PARAMETERS</span></span>

### <span data-ttu-id="6391d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6391d-111">-DefaultProfile</span></span>
<span data-ttu-id="6391d-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6391d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6391d-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6391d-113">-InputObject</span></span>
<span data-ttu-id="6391d-114">Das Eingabeobjekt für das Cmdlet: Das ASR-Netzwerkzuordnungsobjekt, das der zu löschende ASR-Netzwerkzuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="6391d-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

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

### <span data-ttu-id="6391d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6391d-115">-Confirm</span></span>
<span data-ttu-id="6391d-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6391d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6391d-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6391d-117">-WhatIf</span></span>
<span data-ttu-id="6391d-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6391d-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6391d-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6391d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6391d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6391d-120">CommonParameters</span></span>
<span data-ttu-id="6391d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6391d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6391d-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6391d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6391d-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6391d-123">INPUTS</span></span>

### <span data-ttu-id="6391d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6391d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="6391d-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6391d-125">OUTPUTS</span></span>

### <span data-ttu-id="6391d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6391d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6391d-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6391d-127">NOTES</span></span>

## <span data-ttu-id="6391d-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6391d-128">RELATED LINKS</span></span>

[<span data-ttu-id="6391d-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6391d-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="6391d-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6391d-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
