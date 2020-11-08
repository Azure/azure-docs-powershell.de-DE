---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995429"
---
# <span data-ttu-id="5c785-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5c785-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="5c785-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c785-102">SYNOPSIS</span></span>
<span data-ttu-id="5c785-103">Entfernt eine Azure Web-App.</span><span class="sxs-lookup"><span data-stu-id="5c785-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="5c785-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c785-104">SYNTAX</span></span>

### <span data-ttu-id="5c785-105">S1</span><span class="sxs-lookup"><span data-stu-id="5c785-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c785-106">S2</span><span class="sxs-lookup"><span data-stu-id="5c785-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c785-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c785-107">DESCRIPTION</span></span>
<span data-ttu-id="5c785-108">Das Cmdlet **Remove-AzWebApp** entfernt eine Azure Web App, die die Ressourcengruppe und den Namen der Web App bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="5c785-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="5c785-109">Dieses Cmdlet entfernt standardmäßig auch alle Slots und Metriken.</span><span class="sxs-lookup"><span data-stu-id="5c785-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="5c785-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c785-110">EXAMPLES</span></span>

### <span data-ttu-id="5c785-111">Beispiel 1: Entfernen einer Web-App</span><span class="sxs-lookup"><span data-stu-id="5c785-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="5c785-112">Mit diesem Befehl wird die Azure Web App mit dem Namen ContosoSite entfernt, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="5c785-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="5c785-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c785-113">PARAMETERS</span></span>

### <span data-ttu-id="5c785-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c785-114">-AsJob</span></span>
<span data-ttu-id="5c785-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5c785-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c785-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c785-116">-DefaultProfile</span></span>
<span data-ttu-id="5c785-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5c785-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c785-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5c785-118">-Force</span></span>
<span data-ttu-id="5c785-119">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="5c785-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="5c785-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5c785-120">-Name</span></span>
<span data-ttu-id="5c785-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="5c785-121">WebApp Name</span></span>

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

### <span data-ttu-id="5c785-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c785-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c785-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="5c785-123">Resource Group Name</span></span>

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

### <span data-ttu-id="5c785-124">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="5c785-124">-WebApp</span></span>
<span data-ttu-id="5c785-125">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="5c785-125">WebApp Object</span></span>

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

### <span data-ttu-id="5c785-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5c785-126">-Confirm</span></span>
<span data-ttu-id="5c785-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen. Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5c785-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c785-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c785-128">-WhatIf</span></span>
<span data-ttu-id="5c785-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c785-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c785-130">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c785-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c785-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c785-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c785-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c785-132">CommonParameters</span></span>
<span data-ttu-id="5c785-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c785-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c785-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c785-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c785-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c785-135">INPUTS</span></span>

### <span data-ttu-id="5c785-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5c785-136">System.String</span></span>

### <span data-ttu-id="5c785-137">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="5c785-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5c785-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c785-138">OUTPUTS</span></span>

### <span data-ttu-id="5c785-139">System. void</span><span class="sxs-lookup"><span data-stu-id="5c785-139">System.Void</span></span>

## <span data-ttu-id="5c785-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c785-140">NOTES</span></span>

## <span data-ttu-id="5c785-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c785-141">RELATED LINKS</span></span>

[<span data-ttu-id="5c785-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5c785-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="5c785-143">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5c785-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="5c785-144">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5c785-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="5c785-145">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5c785-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="5c785-146">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5c785-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


