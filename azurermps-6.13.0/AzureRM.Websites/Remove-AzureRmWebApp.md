---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b06a5253ac5b26097d2dc4dea9c3d557c00a4d46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477534"
---
# <span data-ttu-id="6d716-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6d716-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="6d716-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d716-102">SYNOPSIS</span></span>
<span data-ttu-id="6d716-103">Entfernt eine Azure Web-App.</span><span class="sxs-lookup"><span data-stu-id="6d716-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d716-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d716-104">SYNTAX</span></span>

### <span data-ttu-id="6d716-105">S1</span><span class="sxs-lookup"><span data-stu-id="6d716-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d716-106">S2</span><span class="sxs-lookup"><span data-stu-id="6d716-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d716-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d716-107">DESCRIPTION</span></span>
<span data-ttu-id="6d716-108">Das Cmdlet **Remove-AzureRmWebApp** entfernt eine Azure Web App, die die Ressourcengruppe und den Namen der Web App bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="6d716-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="6d716-109">Dieses Cmdlet entfernt standardmäßig auch alle Slots und Metriken.</span><span class="sxs-lookup"><span data-stu-id="6d716-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="6d716-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d716-110">EXAMPLES</span></span>

### <span data-ttu-id="6d716-111">Beispiel 1: Entfernen einer Web-App</span><span class="sxs-lookup"><span data-stu-id="6d716-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="6d716-112">Mit diesem Befehl wird die Azure Web App mit dem Namen ContosoSite entfernt, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="6d716-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="6d716-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d716-113">PARAMETERS</span></span>

### <span data-ttu-id="6d716-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d716-114">-AsJob</span></span>
<span data-ttu-id="6d716-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6d716-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d716-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d716-116">-DefaultProfile</span></span>
<span data-ttu-id="6d716-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6d716-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d716-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6d716-118">-Force</span></span>
<span data-ttu-id="6d716-119">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="6d716-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="6d716-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6d716-120">-Name</span></span>
<span data-ttu-id="6d716-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="6d716-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d716-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d716-122">-ResourceGroupName</span></span>
<span data-ttu-id="6d716-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="6d716-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d716-124">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="6d716-124">-WebApp</span></span>
<span data-ttu-id="6d716-125">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="6d716-125">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d716-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6d716-126">-Confirm</span></span>
<span data-ttu-id="6d716-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen. Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d716-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d716-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d716-128">-WhatIf</span></span>
<span data-ttu-id="6d716-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d716-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d716-130">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d716-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d716-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d716-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d716-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d716-132">CommonParameters</span></span>
<span data-ttu-id="6d716-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d716-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d716-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d716-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d716-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d716-135">INPUTS</span></span>

### <span data-ttu-id="6d716-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6d716-136">System.String</span></span>

### <span data-ttu-id="6d716-137">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="6d716-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="6d716-138">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="6d716-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="6d716-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d716-139">OUTPUTS</span></span>

### <span data-ttu-id="6d716-140">System. void</span><span class="sxs-lookup"><span data-stu-id="6d716-140">System.Void</span></span>

## <span data-ttu-id="6d716-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d716-141">NOTES</span></span>

## <span data-ttu-id="6d716-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d716-142">RELATED LINKS</span></span>

[<span data-ttu-id="6d716-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6d716-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="6d716-144">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6d716-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="6d716-145">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6d716-145">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="6d716-146">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6d716-146">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="6d716-147">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6d716-147">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


