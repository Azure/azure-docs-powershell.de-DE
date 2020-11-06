---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 121d45d626a226542f495cd197781b795823b1fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502358"
---
# <span data-ttu-id="c0be7-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c0be7-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="c0be7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0be7-102">SYNOPSIS</span></span>
<span data-ttu-id="c0be7-103">Entfernt ein geschütztes Element der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="c0be7-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0be7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0be7-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0be7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0be7-105">DESCRIPTION</span></span>
<span data-ttu-id="c0be7-106">Das Cmdlet **Remove-AzureRmSiteRecoveryReplicationProtectedItem** entfernt ein geschütztes Element der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="c0be7-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="c0be7-107">Dieser Vorgang bewirkt, dass die Replikation für das geschützte Element beendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0be7-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="c0be7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0be7-108">EXAMPLES</span></span>

## <span data-ttu-id="c0be7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0be7-109">PARAMETERS</span></span>

### <span data-ttu-id="c0be7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0be7-110">-DefaultProfile</span></span>
<span data-ttu-id="c0be7-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0be7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0be7-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c0be7-112">-Force</span></span>
<span data-ttu-id="c0be7-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c0be7-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0be7-114">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c0be7-114">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c0be7-115">Gibt das Objekt mit dem Replikations geschützten Element an.</span><span class="sxs-lookup"><span data-stu-id="c0be7-115">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0be7-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="c0be7-116">-WaitForCompletion</span></span>
<span data-ttu-id="c0be7-117">Gibt an, dass das Cmdlet auf den Abschluss des Vorgangs wartet.</span><span class="sxs-lookup"><span data-stu-id="c0be7-117">Indicates that the cmdlet waits for the operation to complete.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0be7-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0be7-118">-Confirm</span></span>
<span data-ttu-id="c0be7-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0be7-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0be7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0be7-120">-WhatIf</span></span>
<span data-ttu-id="c0be7-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0be7-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c0be7-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0be7-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0be7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0be7-123">CommonParameters</span></span>
<span data-ttu-id="c0be7-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0be7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0be7-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0be7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0be7-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0be7-126">INPUTS</span></span>

### <span data-ttu-id="c0be7-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c0be7-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="c0be7-128">Der Parameter "ReplicationProtectedItem" akzeptiert den Wert vom Typ "ASRReplicationProtectedItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0be7-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="c0be7-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0be7-129">OUTPUTS</span></span>

### <span data-ttu-id="c0be7-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c0be7-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c0be7-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0be7-131">NOTES</span></span>

## <span data-ttu-id="c0be7-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0be7-132">RELATED LINKS</span></span>

[<span data-ttu-id="c0be7-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c0be7-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="c0be7-134">Neu – AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c0be7-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="c0be7-135">Satz-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c0be7-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
