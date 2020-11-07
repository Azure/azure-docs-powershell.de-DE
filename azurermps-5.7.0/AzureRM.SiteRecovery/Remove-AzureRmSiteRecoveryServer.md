---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 7c7afc0a1b6544f165f379a7363960142f73780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664166"
---
# <span data-ttu-id="0c55c-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="0c55c-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="0c55c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c55c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c55c-103">Entfernt einen Standort Wiederherstellungsserver aus dem aktuellen Tresor.</span><span class="sxs-lookup"><span data-stu-id="0c55c-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c55c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c55c-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c55c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c55c-105">DESCRIPTION</span></span>
<span data-ttu-id="0c55c-106">Das Cmdlet **Remove-AzureRmSiteRecoveryServer** hebt die Registrierung eines Azure Site Recovery-Servers auf, der ihn aus dem aktuellen Tresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="0c55c-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="0c55c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c55c-107">EXAMPLES</span></span>

## <span data-ttu-id="0c55c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c55c-108">PARAMETERS</span></span>

### <span data-ttu-id="0c55c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c55c-109">-DefaultProfile</span></span>
<span data-ttu-id="0c55c-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c55c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c55c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0c55c-111">-Force</span></span>
<span data-ttu-id="0c55c-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="0c55c-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c55c-113">-Server</span><span class="sxs-lookup"><span data-stu-id="0c55c-113">-Server</span></span>
<span data-ttu-id="0c55c-114">Gibt das Objekt der Standort Wiederherstellungsserver an.</span><span class="sxs-lookup"><span data-stu-id="0c55c-114">Specifies the Site Recovery server object.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c55c-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0c55c-115">-Confirm</span></span>
<span data-ttu-id="0c55c-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c55c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c55c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c55c-117">-WhatIf</span></span>
<span data-ttu-id="0c55c-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c55c-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0c55c-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c55c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c55c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c55c-120">CommonParameters</span></span>
<span data-ttu-id="0c55c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c55c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c55c-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c55c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c55c-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c55c-123">INPUTS</span></span>

### <span data-ttu-id="0c55c-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="0c55c-124">ASRServer</span></span>
<span data-ttu-id="0c55c-125">Der Parameter "Server" akzeptiert den Wert vom Typ "ASRServer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0c55c-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="0c55c-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c55c-126">OUTPUTS</span></span>

### <span data-ttu-id="0c55c-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="0c55c-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="0c55c-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c55c-128">NOTES</span></span>

## <span data-ttu-id="0c55c-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c55c-129">RELATED LINKS</span></span>

[<span data-ttu-id="0c55c-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="0c55c-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="0c55c-131">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="0c55c-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)
