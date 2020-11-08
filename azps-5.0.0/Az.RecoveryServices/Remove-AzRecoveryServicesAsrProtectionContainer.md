---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178247"
---
# <span data-ttu-id="e3672-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e3672-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="e3672-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3672-102">SYNOPSIS</span></span>
<span data-ttu-id="e3672-103">Löscht den angegebenen Schutz Container aus seiner Struktur.</span><span class="sxs-lookup"><span data-stu-id="e3672-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="e3672-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3672-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3672-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3672-105">DESCRIPTION</span></span>
<span data-ttu-id="e3672-106">Das Remove-AzRecoveryServicesAsrProtectionContainer-Cmdlet löscht den angegebenen Azure Site Recovery Protection-Container.</span><span class="sxs-lookup"><span data-stu-id="e3672-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="e3672-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3672-107">EXAMPLES</span></span>

### <span data-ttu-id="e3672-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e3672-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="e3672-109">Startet den Löschvorgang des angegebenen Schutz Containers und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des entfernen-Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3672-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="e3672-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3672-110">PARAMETERS</span></span>

### <span data-ttu-id="e3672-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3672-111">-DefaultProfile</span></span>
<span data-ttu-id="e3672-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3672-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3672-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e3672-113">-InputObject</span></span>
<span data-ttu-id="e3672-114">Gibt den Schutzcontainer an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3672-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3672-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e3672-115">-Confirm</span></span>
<span data-ttu-id="e3672-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3672-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3672-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3672-117">-WhatIf</span></span>
<span data-ttu-id="e3672-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3672-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3672-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3672-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3672-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3672-120">CommonParameters</span></span>
<span data-ttu-id="e3672-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3672-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3672-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3672-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3672-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3672-123">INPUTS</span></span>

### <span data-ttu-id="e3672-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e3672-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="e3672-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3672-125">OUTPUTS</span></span>

### <span data-ttu-id="e3672-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e3672-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e3672-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3672-127">NOTES</span></span>

## <span data-ttu-id="e3672-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3672-128">RELATED LINKS</span></span>
