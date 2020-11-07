---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 8c168027573c0160519c8600e3e55cac534edeca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841092"
---
# <span data-ttu-id="6b48b-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="6b48b-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="6b48b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b48b-102">SYNOPSIS</span></span>
<span data-ttu-id="6b48b-103">Entscheidet sich, Daten zu sammeln, um die AzurePowerShell-Cmdlets zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="6b48b-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="6b48b-104">Daten werden nicht erfasst, es sei denn, Sie entscheiden sich ausdrücklich dafür.</span><span class="sxs-lookup"><span data-stu-id="6b48b-104">Data is not collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="6b48b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b48b-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b48b-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b48b-106">DESCRIPTION</span></span>
<span data-ttu-id="6b48b-107">Sie können die Nutzung der Microsoft-Cloud und Azure PowerShell verbessern, indem Sie sich für die Datensammlung entscheiden.</span><span class="sxs-lookup"><span data-stu-id="6b48b-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="6b48b-108">Azure PowerShell sammelt keine Daten ohne Ihre Zustimmung – Sie müssen sich explizit durch Ausführen von enable-AzDataCollection oder durch die Beantwortung von "Ja" anmelden, wenn Azure PowerShell Sie zum ersten Mal beim Ausführen eines Cmdlets auffordert, Daten zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="6b48b-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="6b48b-109">Microsoft aggregiert gesammelte Daten, um Nutzungsmuster zu identifizieren, häufige Probleme zu erkennen und die Nutzung von Azure PowerShell zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="6b48b-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="6b48b-110">Microsoft Azure PowerShell sammelt keine privaten Daten oder keine persönlich identifizierbaren Informationen.</span><span class="sxs-lookup"><span data-stu-id="6b48b-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="6b48b-111">Führen Sie das Disable-AzDataCollection-Cmdlet aus, um die Datensammlung für den aktuellen Benutzer zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6b48b-111">Run the Disable-AzDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="6b48b-112">Dadurch wird verhindert, dass der aktuelle Benutzer zur Datensammlung aufgefordert wird, wenn Cmdlets erstmalig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6b48b-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="6b48b-113">Wenn Sie die Datensammlung für den aktuellen Benutzer aktivieren möchten, führen Sie das Enable-AzDataCollection-Cmdlet aus.</span><span class="sxs-lookup"><span data-stu-id="6b48b-113">To enable data collection for the current user, run the Enable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="6b48b-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b48b-114">EXAMPLES</span></span>

### <span data-ttu-id="6b48b-115">Beispiel 1: Deaktivieren der Datensammlung für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="6b48b-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzDataCollection
```

<span data-ttu-id="6b48b-116">In diesem Beispiel wird gezeigt, wie Sie die Datensammlung für den aktuellen Benutzer deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6b48b-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="6b48b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b48b-117">PARAMETERS</span></span>

### <span data-ttu-id="6b48b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b48b-118">-DefaultProfile</span></span>
<span data-ttu-id="6b48b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6b48b-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b48b-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6b48b-120">-Confirm</span></span>
<span data-ttu-id="6b48b-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b48b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b48b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b48b-122">-WhatIf</span></span>
<span data-ttu-id="6b48b-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b48b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b48b-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b48b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b48b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b48b-125">CommonParameters</span></span>
<span data-ttu-id="6b48b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b48b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b48b-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b48b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b48b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b48b-128">INPUTS</span></span>

### <span data-ttu-id="6b48b-129">Keine</span><span class="sxs-lookup"><span data-stu-id="6b48b-129">None</span></span>

## <span data-ttu-id="6b48b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b48b-130">OUTPUTS</span></span>

### <span data-ttu-id="6b48b-131">System. void</span><span class="sxs-lookup"><span data-stu-id="6b48b-131">System.Void</span></span>

## <span data-ttu-id="6b48b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b48b-132">NOTES</span></span>

## <span data-ttu-id="6b48b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b48b-133">RELATED LINKS</span></span>

[<span data-ttu-id="6b48b-134">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="6b48b-134">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)

