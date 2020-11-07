---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: e4e6579c330f8ac4189db2ddfc5d3a0578fd07f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825272"
---
# <span data-ttu-id="0cb6b-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0cb6b-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="0cb6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0cb6b-102">SYNOPSIS</span></span>
<span data-ttu-id="0cb6b-103">Löscht die angegebene ASR-Netzwerkzuordnung aus dem Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="0cb6b-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="0cb6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cb6b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cb6b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0cb6b-105">DESCRIPTION</span></span>
<span data-ttu-id="0cb6b-106">Das Cmdlet **Remove-AzRecoveryServicesAsrNetworkMapping** löscht die angegebene ASR-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="0cb6b-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="0cb6b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0cb6b-107">EXAMPLES</span></span>

### <span data-ttu-id="0cb6b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0cb6b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="0cb6b-109">Startet das Löschen der angegebenen ASR-Netzwerkzuordnung und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0cb6b-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0cb6b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cb6b-110">PARAMETERS</span></span>

### <span data-ttu-id="0cb6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cb6b-111">-DefaultProfile</span></span>
<span data-ttu-id="0cb6b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0cb6b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0cb6b-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0cb6b-113">-InputObject</span></span>
<span data-ttu-id="0cb6b-114">Das Eingabeobjekt für das Cmdlet: das ASR-Netzwerk Zuordnungsobjekt, das der zu löschenden ASR-Netzwerkzuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="0cb6b-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

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

### <span data-ttu-id="0cb6b-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0cb6b-115">-Confirm</span></span>
<span data-ttu-id="0cb6b-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0cb6b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cb6b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cb6b-117">-WhatIf</span></span>
<span data-ttu-id="0cb6b-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0cb6b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0cb6b-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0cb6b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cb6b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cb6b-120">CommonParameters</span></span>
<span data-ttu-id="0cb6b-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cb6b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cb6b-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cb6b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cb6b-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0cb6b-123">INPUTS</span></span>

### <span data-ttu-id="0cb6b-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0cb6b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="0cb6b-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0cb6b-125">OUTPUTS</span></span>

### <span data-ttu-id="0cb6b-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0cb6b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0cb6b-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="0cb6b-127">NOTES</span></span>

## <span data-ttu-id="0cb6b-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0cb6b-128">RELATED LINKS</span></span>

[<span data-ttu-id="0cb6b-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0cb6b-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="0cb6b-130">Neu – AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0cb6b-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
