---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 20a57bd70c9cf9b1b533e040001afee0cc5809fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659847"
---
# <span data-ttu-id="b2499-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b2499-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="b2499-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2499-102">SYNOPSIS</span></span>
<span data-ttu-id="b2499-103">Löscht den angegebenen Schutz Container aus seiner Struktur.</span><span class="sxs-lookup"><span data-stu-id="b2499-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="b2499-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2499-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2499-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2499-105">DESCRIPTION</span></span>
<span data-ttu-id="b2499-106">Das Remove-AzRecoveryServicesAsrProtectionContainer-Cmdlet löscht den angegebenen Azure Site Recovery Protection-Container.</span><span class="sxs-lookup"><span data-stu-id="b2499-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="b2499-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2499-107">EXAMPLES</span></span>

### <span data-ttu-id="b2499-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b2499-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="b2499-109">Startet den Löschvorgang des angegebenen Schutz Containers und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des entfernen-Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2499-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="b2499-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2499-110">PARAMETERS</span></span>

### <span data-ttu-id="b2499-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2499-111">-DefaultProfile</span></span>
<span data-ttu-id="b2499-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2499-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2499-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b2499-113">-InputObject</span></span>
<span data-ttu-id="b2499-114">Gibt den Schutzcontainer an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2499-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="b2499-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2499-115">-Confirm</span></span>
<span data-ttu-id="b2499-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2499-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2499-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2499-117">-WhatIf</span></span>
<span data-ttu-id="b2499-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2499-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2499-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2499-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2499-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2499-120">CommonParameters</span></span>
<span data-ttu-id="b2499-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2499-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2499-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2499-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2499-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2499-123">INPUTS</span></span>

### <span data-ttu-id="b2499-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b2499-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="b2499-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2499-125">OUTPUTS</span></span>

### <span data-ttu-id="b2499-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b2499-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b2499-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2499-127">NOTES</span></span>

## <span data-ttu-id="b2499-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2499-128">RELATED LINKS</span></span>
