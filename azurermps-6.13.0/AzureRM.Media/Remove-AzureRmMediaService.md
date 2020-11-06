---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/remove-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 9ddf8291d5f6276126cea82305bbc554d05ca006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503585"
---
# <span data-ttu-id="cd114-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="cd114-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="cd114-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd114-102">SYNOPSIS</span></span>
<span data-ttu-id="cd114-103">Entfernt einen Mediendienst.</span><span class="sxs-lookup"><span data-stu-id="cd114-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd114-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd114-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd114-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd114-105">DESCRIPTION</span></span>
<span data-ttu-id="cd114-106">Mit dem Cmdlet **Remove-AzureRmMediaService** wird ein Mediendienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd114-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="cd114-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd114-107">EXAMPLES</span></span>

### <span data-ttu-id="cd114-108">Beispiel 1: Entfernen eines Medien Diensts</span><span class="sxs-lookup"><span data-stu-id="cd114-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="cd114-109">Dieser Befehl entfernt den Mediendienst mit dem Namen MediaService0011 in der Ressourcengruppe mit dem Namen ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="cd114-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="cd114-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd114-110">PARAMETERS</span></span>

### <span data-ttu-id="cd114-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="cd114-111">-AccountName</span></span>
<span data-ttu-id="cd114-112">Gibt den Namen des Medien Diensts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd114-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cd114-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd114-113">-DefaultProfile</span></span>
<span data-ttu-id="cd114-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cd114-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd114-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cd114-115">-Force</span></span>
<span data-ttu-id="cd114-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="cd114-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd114-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd114-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd114-118">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="cd114-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="cd114-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cd114-119">-Confirm</span></span>
<span data-ttu-id="cd114-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd114-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd114-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd114-121">-WhatIf</span></span>
<span data-ttu-id="cd114-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd114-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd114-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd114-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd114-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd114-124">CommonParameters</span></span>
<span data-ttu-id="cd114-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd114-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd114-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd114-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd114-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd114-127">INPUTS</span></span>

### <span data-ttu-id="cd114-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cd114-128">System.String</span></span>

## <span data-ttu-id="cd114-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd114-129">OUTPUTS</span></span>

### <span data-ttu-id="cd114-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd114-130">System.Boolean</span></span>

## <span data-ttu-id="cd114-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd114-131">NOTES</span></span>

## <span data-ttu-id="cd114-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd114-132">RELATED LINKS</span></span>

[<span data-ttu-id="cd114-133">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="cd114-133">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="cd114-134">Neu – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="cd114-134">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="cd114-135">Satz-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="cd114-135">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


