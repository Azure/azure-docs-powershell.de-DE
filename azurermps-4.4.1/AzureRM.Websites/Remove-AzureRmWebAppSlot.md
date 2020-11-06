---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 65393bc3dd2e9e6b51699a21baf0e6d3750464bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504658"
---
# <span data-ttu-id="e7a61-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7a61-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="e7a61-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7a61-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7a61-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7a61-103">SYNTAX</span></span>

### <span data-ttu-id="e7a61-104">S1</span><span class="sxs-lookup"><span data-stu-id="e7a61-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7a61-105">S2</span><span class="sxs-lookup"><span data-stu-id="e7a61-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7a61-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7a61-106">DESCRIPTION</span></span>
<span data-ttu-id="e7a61-107">Mit dem Cmdlet **Remove-AzureRmWebAppSlot** wird ein Azure Web App-Steckplatz entfernt, vorausgesetzt, die Ressourcengruppe und der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="e7a61-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="e7a61-108">Dieses Cmdlet entfernt standardmäßig auch alle Slots und Metriken.</span><span class="sxs-lookup"><span data-stu-id="e7a61-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="e7a61-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7a61-109">EXAMPLES</span></span>

### <span data-ttu-id="e7a61-110">Beispiel 1: Entfernen eines Web App-Slots</span><span class="sxs-lookup"><span data-stu-id="e7a61-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="e7a61-111">Mit diesem Befehl wird der Steckplatz mit dem Namen "Slot001" entfernt, der Web App-ContosoSite zugeordnet ist, die zu der Ressourcengruppe "Default-Web-westus" gehört.</span><span class="sxs-lookup"><span data-stu-id="e7a61-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e7a61-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7a61-112">PARAMETERS</span></span>

### <span data-ttu-id="e7a61-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e7a61-113">-Force</span></span>
<span data-ttu-id="e7a61-114">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="e7a61-114">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="e7a61-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e7a61-115">-Name</span></span>
<span data-ttu-id="e7a61-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="e7a61-116">WebApp Name</span></span>

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

### <span data-ttu-id="e7a61-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a61-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7a61-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="e7a61-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e7a61-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="e7a61-119">-Slot</span></span>
<span data-ttu-id="e7a61-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="e7a61-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a61-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="e7a61-121">-WebApp</span></span>
<span data-ttu-id="e7a61-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="e7a61-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a61-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7a61-123">-Confirm</span></span>
<span data-ttu-id="e7a61-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7a61-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a61-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7a61-125">-WhatIf</span></span>
<span data-ttu-id="e7a61-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7a61-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7a61-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7a61-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a61-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a61-128">-DefaultProfile</span></span>
<span data-ttu-id="e7a61-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7a61-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7a61-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a61-130">CommonParameters</span></span>
<span data-ttu-id="e7a61-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a61-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a61-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7a61-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a61-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7a61-133">INPUTS</span></span>

### <span data-ttu-id="e7a61-134">Website</span><span class="sxs-lookup"><span data-stu-id="e7a61-134">Site</span></span>
<span data-ttu-id="e7a61-135">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e7a61-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e7a61-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7a61-136">OUTPUTS</span></span>

### <span data-ttu-id="e7a61-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e7a61-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e7a61-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7a61-138">NOTES</span></span>

## <span data-ttu-id="e7a61-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7a61-139">RELATED LINKS</span></span>

[<span data-ttu-id="e7a61-140">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7a61-140">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="e7a61-141">Neu – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7a61-141">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="e7a61-142">Neustart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7a61-142">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="e7a61-143">Satz-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7a61-143">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="e7a61-144">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7a61-144">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="e7a61-145">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7a61-145">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="e7a61-146">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e7a61-146">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
