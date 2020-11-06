---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/remove-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 373647cfc06c36a510a8208424d00087f00e693e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476726"
---
# <span data-ttu-id="fb445-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="fb445-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="fb445-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb445-102">SYNOPSIS</span></span>
<span data-ttu-id="fb445-103">Entfernt einen Mediendienst.</span><span class="sxs-lookup"><span data-stu-id="fb445-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb445-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb445-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb445-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb445-105">DESCRIPTION</span></span>
<span data-ttu-id="fb445-106">Mit dem Cmdlet **Remove-AzureRmMediaService** wird ein Mediendienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb445-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="fb445-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb445-107">EXAMPLES</span></span>

### <span data-ttu-id="fb445-108">Beispiel 1: Entfernen eines Medien Diensts</span><span class="sxs-lookup"><span data-stu-id="fb445-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="fb445-109">Dieser Befehl entfernt den Mediendienst mit dem Namen MediaService0011 in der Ressourcengruppe mit dem Namen ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="fb445-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="fb445-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb445-110">PARAMETERS</span></span>

### <span data-ttu-id="fb445-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="fb445-111">-AccountName</span></span>
<span data-ttu-id="fb445-112">Gibt den Namen des Medien Diensts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb445-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb445-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb445-113">-DefaultProfile</span></span>
<span data-ttu-id="fb445-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fb445-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb445-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fb445-115">-Force</span></span>
<span data-ttu-id="fb445-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="fb445-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb445-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb445-117">-ResourceGroupName</span></span>
<span data-ttu-id="fb445-118">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="fb445-118">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb445-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb445-119">-Confirm</span></span>
<span data-ttu-id="fb445-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb445-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb445-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb445-121">-WhatIf</span></span>
<span data-ttu-id="fb445-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb445-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb445-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb445-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb445-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb445-124">CommonParameters</span></span>
<span data-ttu-id="fb445-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb445-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb445-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb445-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb445-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb445-127">INPUTS</span></span>

### <span data-ttu-id="fb445-128">Keine</span><span class="sxs-lookup"><span data-stu-id="fb445-128">None</span></span>
<span data-ttu-id="fb445-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="fb445-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb445-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb445-130">OUTPUTS</span></span>

### <span data-ttu-id="fb445-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb445-131">System.Boolean</span></span>

## <span data-ttu-id="fb445-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb445-132">NOTES</span></span>

## <span data-ttu-id="fb445-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb445-133">RELATED LINKS</span></span>

[<span data-ttu-id="fb445-134">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="fb445-134">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="fb445-135">Neu – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="fb445-135">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="fb445-136">Satz-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="fb445-136">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


