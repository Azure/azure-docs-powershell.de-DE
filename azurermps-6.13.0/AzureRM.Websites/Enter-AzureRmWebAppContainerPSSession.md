---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 350ad76952a2953a107e0626b9cf2e0e8b640bb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477546"
---
# <span data-ttu-id="37061-101">Enter-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="37061-101">Enter-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="37061-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37061-102">SYNOPSIS</span></span>
<span data-ttu-id="37061-103">Öffnet eine PowerShell-Remotesitzung in dem Windows-Container, der in einer bestimmten Website oder in einem bestimmten Steckplatz und einer gegebenen Ressourcengruppe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="37061-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37061-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37061-104">SYNTAX</span></span>

### <span data-ttu-id="37061-105">S1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="37061-105">S1 (Default)</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37061-106">S2</span><span class="sxs-lookup"><span data-stu-id="37061-106">S2</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37061-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37061-107">DESCRIPTION</span></span>
<span data-ttu-id="37061-108">Öffnet eine PowerShell-Remotesitzung in dem Windows-Container, der in einer bestimmten Website oder in einem bestimmten Steckplatz und einer gegebenen Ressourcengruppe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="37061-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="37061-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37061-109">EXAMPLES</span></span>

### <span data-ttu-id="37061-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37061-110">Example 1</span></span>
```
PS C:\> Enter-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="37061-111">Mit diesem Befehl wird eine Remote-PowerShell-Sitzung in der Windows-Container-App ContosoASP</span><span class="sxs-lookup"><span data-stu-id="37061-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="37061-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="37061-112">PARAMETERS</span></span>

### <span data-ttu-id="37061-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37061-113">-DefaultProfile</span></span>
<span data-ttu-id="37061-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37061-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37061-115">-Force</span><span class="sxs-lookup"><span data-stu-id="37061-115">-Force</span></span>
<span data-ttu-id="37061-116">Erstellen Sie die PowerShell-Sitzung ohne Aufforderung zur Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="37061-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="37061-117">-Name</span><span class="sxs-lookup"><span data-stu-id="37061-117">-Name</span></span>
<span data-ttu-id="37061-118">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="37061-118">The name of the web app.</span></span>

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

### <span data-ttu-id="37061-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37061-119">-PassThru</span></span>
<span data-ttu-id="37061-120">Zurückgeben eines Werts, der auf Erfolg oder Fehler hinweist</span><span class="sxs-lookup"><span data-stu-id="37061-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="37061-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37061-121">-ResourceGroupName</span></span>
<span data-ttu-id="37061-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="37061-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="37061-123">-Slotname</span><span class="sxs-lookup"><span data-stu-id="37061-123">-SlotName</span></span>
<span data-ttu-id="37061-124">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="37061-124">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37061-125">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="37061-125">-WebApp</span></span>
<span data-ttu-id="37061-126">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="37061-126">The web app object</span></span>

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

### <span data-ttu-id="37061-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37061-127">-Confirm</span></span>
<span data-ttu-id="37061-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37061-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37061-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37061-129">-WhatIf</span></span>
<span data-ttu-id="37061-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37061-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37061-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37061-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37061-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37061-132">CommonParameters</span></span>
<span data-ttu-id="37061-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37061-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37061-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37061-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37061-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37061-135">INPUTS</span></span>

### <span data-ttu-id="37061-136">System. String</span><span class="sxs-lookup"><span data-stu-id="37061-136">System.String</span></span>
### <span data-ttu-id="37061-137">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="37061-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="37061-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37061-138">OUTPUTS</span></span>

### <span data-ttu-id="37061-139">System. String</span><span class="sxs-lookup"><span data-stu-id="37061-139">System.String</span></span>
## <span data-ttu-id="37061-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="37061-140">NOTES</span></span>

## <span data-ttu-id="37061-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37061-141">RELATED LINKS</span></span>
