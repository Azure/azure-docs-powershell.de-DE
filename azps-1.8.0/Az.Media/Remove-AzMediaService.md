---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: f9d0ee722f828aba251c9776c231338b54c0580c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819060"
---
# <span data-ttu-id="dc2b9-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="dc2b9-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="dc2b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc2b9-102">SYNOPSIS</span></span>
<span data-ttu-id="dc2b9-103">Entfernt einen Mediendienst.</span><span class="sxs-lookup"><span data-stu-id="dc2b9-103">Removes a media service.</span></span>

## <span data-ttu-id="dc2b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc2b9-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc2b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc2b9-105">DESCRIPTION</span></span>
<span data-ttu-id="dc2b9-106">Mit dem Cmdlet **Remove-AzMediaService** wird ein Mediendienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="dc2b9-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="dc2b9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc2b9-107">EXAMPLES</span></span>

### <span data-ttu-id="dc2b9-108">Beispiel 1: Entfernen eines Medien Diensts</span><span class="sxs-lookup"><span data-stu-id="dc2b9-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="dc2b9-109">Dieser Befehl entfernt den Mediendienst mit dem Namen MediaService0011 in der Ressourcengruppe mit dem Namen ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="dc2b9-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="dc2b9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc2b9-110">PARAMETERS</span></span>

### <span data-ttu-id="dc2b9-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="dc2b9-111">-AccountName</span></span>
<span data-ttu-id="dc2b9-112">Gibt den Namen des Medien Diensts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="dc2b9-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc2b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc2b9-113">-DefaultProfile</span></span>
<span data-ttu-id="dc2b9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dc2b9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc2b9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dc2b9-115">-Force</span></span>
<span data-ttu-id="dc2b9-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="dc2b9-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dc2b9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc2b9-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc2b9-118">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="dc2b9-118">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc2b9-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dc2b9-119">-Confirm</span></span>
<span data-ttu-id="dc2b9-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc2b9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc2b9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc2b9-121">-WhatIf</span></span>
<span data-ttu-id="dc2b9-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc2b9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc2b9-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc2b9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc2b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc2b9-124">CommonParameters</span></span>
<span data-ttu-id="dc2b9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc2b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc2b9-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc2b9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc2b9-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc2b9-127">INPUTS</span></span>

### <span data-ttu-id="dc2b9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dc2b9-128">System.String</span></span>

## <span data-ttu-id="dc2b9-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc2b9-129">OUTPUTS</span></span>

### <span data-ttu-id="dc2b9-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc2b9-130">System.Boolean</span></span>

## <span data-ttu-id="dc2b9-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc2b9-131">NOTES</span></span>

## <span data-ttu-id="dc2b9-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc2b9-132">RELATED LINKS</span></span>

[<span data-ttu-id="dc2b9-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="dc2b9-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="dc2b9-134">Neu – AzMediaService</span><span class="sxs-lookup"><span data-stu-id="dc2b9-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="dc2b9-135">Satz-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="dc2b9-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


