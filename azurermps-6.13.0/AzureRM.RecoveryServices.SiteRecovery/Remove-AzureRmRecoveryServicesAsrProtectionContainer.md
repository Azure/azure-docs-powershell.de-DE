---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 0cc4a1c58349157024f38bce6e5ee2d8bcaa3cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503446"
---
# <span data-ttu-id="43998-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="43998-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="43998-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43998-102">SYNOPSIS</span></span>
<span data-ttu-id="43998-103">Löscht den angegebenen Schutz Container aus seiner Struktur.</span><span class="sxs-lookup"><span data-stu-id="43998-103">Deletes the specified Protection Container from its Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43998-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43998-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43998-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43998-105">DESCRIPTION</span></span>
<span data-ttu-id="43998-106">Das Remove-AzureRmRecoveryServicesAsrProtectionContainer-Cmdlet löscht den angegebenen Azure Site Recovery Protection-Container.</span><span class="sxs-lookup"><span data-stu-id="43998-106">The Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="43998-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43998-107">EXAMPLES</span></span>

### <span data-ttu-id="43998-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43998-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="43998-109">Startet den Löschvorgang des angegebenen Schutz Containers und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des entfernen-Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="43998-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="43998-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="43998-110">PARAMETERS</span></span>

### <span data-ttu-id="43998-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43998-111">-DefaultProfile</span></span>
<span data-ttu-id="43998-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43998-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43998-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43998-113">-InputObject</span></span>
<span data-ttu-id="43998-114">Gibt den Schutzcontainer an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="43998-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="43998-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43998-115">-Confirm</span></span>
<span data-ttu-id="43998-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43998-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43998-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43998-117">-WhatIf</span></span>
<span data-ttu-id="43998-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43998-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43998-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43998-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43998-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43998-120">CommonParameters</span></span>
<span data-ttu-id="43998-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43998-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43998-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43998-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43998-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43998-123">INPUTS</span></span>

### <span data-ttu-id="43998-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="43998-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="43998-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43998-125">OUTPUTS</span></span>

### <span data-ttu-id="43998-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="43998-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="43998-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="43998-127">NOTES</span></span>

## <span data-ttu-id="43998-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43998-128">RELATED LINKS</span></span>
