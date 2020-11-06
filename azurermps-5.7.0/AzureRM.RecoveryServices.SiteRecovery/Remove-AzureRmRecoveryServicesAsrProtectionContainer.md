---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 496eeed8b4ed4b41ce2c67d47fc636711cd5cb84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482845"
---
# <span data-ttu-id="13a0e-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="13a0e-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="13a0e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="13a0e-103">Löscht den angegebenen Schutz Container aus seiner Struktur.</span><span class="sxs-lookup"><span data-stu-id="13a0e-103">Deletes the specified Protection Container from its Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13a0e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13a0e-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13a0e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13a0e-105">DESCRIPTION</span></span>
<span data-ttu-id="13a0e-106">Das Remove-AzureRmRecoveryServicesAsrProtectionContainer-Cmdlet löscht den angegebenen Azure Site Recovery Protection-Container.</span><span class="sxs-lookup"><span data-stu-id="13a0e-106">The Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="13a0e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13a0e-107">EXAMPLES</span></span>

### <span data-ttu-id="13a0e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13a0e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="13a0e-109">Startet den Löschvorgang des angegebenen Schutz Containers und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des entfernen-Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13a0e-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="13a0e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="13a0e-110">PARAMETERS</span></span>

### <span data-ttu-id="13a0e-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="13a0e-111">-Confirm</span></span>
<span data-ttu-id="13a0e-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13a0e-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13a0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a0e-113">-DefaultProfile</span></span>
<span data-ttu-id="13a0e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13a0e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13a0e-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="13a0e-115">-InputObject</span></span>
<span data-ttu-id="13a0e-116">Gibt den Schutzcontainer an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="13a0e-116">Specifies the protection container to be removed .</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13a0e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13a0e-117">-WhatIf</span></span>
<span data-ttu-id="13a0e-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13a0e-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13a0e-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13a0e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13a0e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a0e-120">CommonParameters</span></span>
<span data-ttu-id="13a0e-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13a0e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a0e-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a0e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a0e-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13a0e-123">INPUTS</span></span>

### <span data-ttu-id="13a0e-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="13a0e-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="13a0e-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13a0e-125">OUTPUTS</span></span>

### <span data-ttu-id="13a0e-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="13a0e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="13a0e-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="13a0e-127">NOTES</span></span>

## <span data-ttu-id="13a0e-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13a0e-128">RELATED LINKS</span></span>
