---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 4be04d590adbf75760472f4047b7de9efcffd2d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664974"
---
# <span data-ttu-id="d33f5-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="d33f5-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="d33f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d33f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d33f5-103">Entfernt einen Standort Wiederherstellungsserver aus dem aktuellen Tresor.</span><span class="sxs-lookup"><span data-stu-id="d33f5-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d33f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d33f5-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d33f5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d33f5-105">DESCRIPTION</span></span>
<span data-ttu-id="d33f5-106">Das Cmdlet **Remove-AzureRmSiteRecoveryServer** hebt die Registrierung eines Azure Site Recovery-Servers auf, der ihn aus dem aktuellen Tresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="d33f5-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="d33f5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d33f5-107">EXAMPLES</span></span>

## <span data-ttu-id="d33f5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d33f5-108">PARAMETERS</span></span>

### <span data-ttu-id="d33f5-109">-Force</span><span class="sxs-lookup"><span data-stu-id="d33f5-109">-Force</span></span>
<span data-ttu-id="d33f5-110">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d33f5-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d33f5-111">-Server</span><span class="sxs-lookup"><span data-stu-id="d33f5-111">-Server</span></span>
<span data-ttu-id="d33f5-112">Gibt das Objekt der Standort Wiederherstellungsserver an.</span><span class="sxs-lookup"><span data-stu-id="d33f5-112">Specifies the Site Recovery server object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d33f5-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d33f5-113">-Confirm</span></span>
<span data-ttu-id="d33f5-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d33f5-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d33f5-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d33f5-115">-WhatIf</span></span>
<span data-ttu-id="d33f5-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d33f5-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d33f5-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d33f5-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d33f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d33f5-118">-DefaultProfile</span></span>
<span data-ttu-id="d33f5-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d33f5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d33f5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d33f5-120">CommonParameters</span></span>
<span data-ttu-id="d33f5-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d33f5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d33f5-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d33f5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d33f5-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d33f5-123">INPUTS</span></span>

### <span data-ttu-id="d33f5-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="d33f5-124">ASRServer</span></span>
<span data-ttu-id="d33f5-125">Der Parameter "Server" akzeptiert den Wert vom Typ "ASRServer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d33f5-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="d33f5-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d33f5-126">OUTPUTS</span></span>

### <span data-ttu-id="d33f5-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="d33f5-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="d33f5-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="d33f5-128">NOTES</span></span>

## <span data-ttu-id="d33f5-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d33f5-129">RELATED LINKS</span></span>

[<span data-ttu-id="d33f5-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="d33f5-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="d33f5-131">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="d33f5-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)
