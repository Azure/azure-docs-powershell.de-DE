---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e1d5dd0c8548b52fde37044d304269358a11af70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664421"
---
# <span data-ttu-id="49896-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="49896-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="49896-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49896-102">SYNOPSIS</span></span>
<span data-ttu-id="49896-103">Entfernt ein geschütztes Element der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="49896-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49896-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49896-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49896-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49896-105">DESCRIPTION</span></span>
<span data-ttu-id="49896-106">Das Cmdlet **Remove-AzureRmSiteRecoveryReplicationProtectedItem** entfernt ein geschütztes Element der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="49896-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="49896-107">Dieser Vorgang bewirkt, dass die Replikation für das geschützte Element beendet wird.</span><span class="sxs-lookup"><span data-stu-id="49896-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="49896-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49896-108">EXAMPLES</span></span>

## <span data-ttu-id="49896-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="49896-109">PARAMETERS</span></span>

### <span data-ttu-id="49896-110">-Force</span><span class="sxs-lookup"><span data-stu-id="49896-110">-Force</span></span>
<span data-ttu-id="49896-111">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="49896-111">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49896-112">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="49896-112">-ReplicationProtectedItem</span></span>
<span data-ttu-id="49896-113">Gibt das Objekt mit dem Replikations geschützten Element an.</span><span class="sxs-lookup"><span data-stu-id="49896-113">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49896-114">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="49896-114">-WaitForCompletion</span></span>
<span data-ttu-id="49896-115">Gibt an, dass das Cmdlet auf den Abschluss des Vorgangs wartet.</span><span class="sxs-lookup"><span data-stu-id="49896-115">Indicates that the cmdlet waits for the operation to complete.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49896-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="49896-116">-Confirm</span></span>
<span data-ttu-id="49896-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49896-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49896-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49896-118">-WhatIf</span></span>
<span data-ttu-id="49896-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49896-119">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="49896-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49896-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49896-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49896-121">-DefaultProfile</span></span>
<span data-ttu-id="49896-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49896-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49896-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49896-123">CommonParameters</span></span>
<span data-ttu-id="49896-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49896-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49896-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49896-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49896-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49896-126">INPUTS</span></span>

### <span data-ttu-id="49896-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="49896-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="49896-128">Der Parameter "ReplicationProtectedItem" akzeptiert den Wert vom Typ "ASRReplicationProtectedItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="49896-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="49896-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49896-129">OUTPUTS</span></span>

### <span data-ttu-id="49896-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="49896-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="49896-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="49896-131">NOTES</span></span>

## <span data-ttu-id="49896-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49896-132">RELATED LINKS</span></span>

[<span data-ttu-id="49896-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="49896-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="49896-134">Neu – AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="49896-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="49896-135">Satz-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="49896-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
