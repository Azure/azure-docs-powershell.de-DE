---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a51be31c510d7e428ced0c9ce5ab73a80ab28f75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478297"
---
# <span data-ttu-id="7b142-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7b142-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="7b142-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b142-102">SYNOPSIS</span></span>
<span data-ttu-id="7b142-103">Löscht die angegebene ASR-Netzwerkzuordnung aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="7b142-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b142-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b142-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b142-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b142-105">DESCRIPTION</span></span>
<span data-ttu-id="7b142-106">Das Cmdlet **Remove-AzureRmRecoveryServicesAsrNetworkMapping** löscht die angegebene ASR-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="7b142-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="7b142-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b142-107">EXAMPLES</span></span>

### <span data-ttu-id="7b142-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7b142-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="7b142-109">Startet das Löschen der angegebenen ASR-Netzwerkzuordnung und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b142-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7b142-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b142-110">PARAMETERS</span></span>

### <span data-ttu-id="7b142-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7b142-111">-Confirm</span></span>
<span data-ttu-id="7b142-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b142-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b142-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b142-113">-DefaultProfile</span></span>
<span data-ttu-id="7b142-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b142-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="7b142-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7b142-115">-InputObject</span></span>
<span data-ttu-id="7b142-116">Das Eingabeobjekt für das Cmdlet: das ASR-Netzwerk Zuordnungsobjekt, das der zu löschenden ASR-Netzwerkzuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="7b142-116">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b142-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b142-117">-WhatIf</span></span>
<span data-ttu-id="7b142-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b142-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b142-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b142-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b142-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b142-120">CommonParameters</span></span>
<span data-ttu-id="7b142-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b142-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b142-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b142-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b142-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b142-123">INPUTS</span></span>

### <span data-ttu-id="7b142-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7b142-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="7b142-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b142-125">OUTPUTS</span></span>

### <span data-ttu-id="7b142-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7b142-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7b142-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b142-127">NOTES</span></span>

## <span data-ttu-id="7b142-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b142-128">RELATED LINKS</span></span>

[<span data-ttu-id="7b142-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7b142-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="7b142-130">Neu – AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7b142-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
