---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 651ca91a8da5a025040127b4e3bbcedf16225faf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823072"
---
# <span data-ttu-id="0fd3d-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="0fd3d-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="0fd3d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0fd3d-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd3d-103">New-AzWebAppContainerPSSession erstellt eine neue Remote-PowerShell-Sitzung in dem Windows-Container, der in einer bestimmten Website oder in einem bestimmten Steckplatz und einer gegebenen Ressourcengruppe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="0fd3d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fd3d-104">SYNTAX</span></span>

### <span data-ttu-id="0fd3d-105">S1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="0fd3d-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fd3d-106">S2</span><span class="sxs-lookup"><span data-stu-id="0fd3d-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fd3d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fd3d-107">DESCRIPTION</span></span>
<span data-ttu-id="0fd3d-108">New-AzWebAppContainerPSSession erstellt eine neue Remote-PowerShell-Sitzung in dem Windows-Container, der in einer bestimmten Website oder in einem bestimmten Steckplatz und einer gegebenen Ressourcengruppe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="0fd3d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fd3d-109">EXAMPLES</span></span>

### <span data-ttu-id="0fd3d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0fd3d-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="0fd3d-111">Dadurch wird eine neue Remote-PowerShell-Sitzung in der Windows-Container-App ContosoASP erstellt und die Prozesse angezeigt, die auf dem Container ausgeführt werden ContosoASP</span><span class="sxs-lookup"><span data-stu-id="0fd3d-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="0fd3d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fd3d-112">PARAMETERS</span></span>

### <span data-ttu-id="0fd3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd3d-113">-DefaultProfile</span></span>
<span data-ttu-id="0fd3d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fd3d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0fd3d-115">-Force</span></span>
<span data-ttu-id="0fd3d-116">Erstellen Sie die PowerShell-Sitzung ohne Aufforderung zur Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0fd3d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0fd3d-117">-Name</span></span>
<span data-ttu-id="0fd3d-118">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-118">The name of the web app.</span></span>

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

### <span data-ttu-id="0fd3d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fd3d-119">-ResourceGroupName</span></span>
<span data-ttu-id="0fd3d-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="0fd3d-121">-Slotname</span><span class="sxs-lookup"><span data-stu-id="0fd3d-121">-SlotName</span></span>
<span data-ttu-id="0fd3d-122">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="0fd3d-123">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="0fd3d-123">-WebApp</span></span>
<span data-ttu-id="0fd3d-124">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="0fd3d-124">The web app object</span></span>

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

### <span data-ttu-id="0fd3d-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0fd3d-125">-Confirm</span></span>
<span data-ttu-id="0fd3d-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fd3d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fd3d-127">-WhatIf</span></span>
<span data-ttu-id="0fd3d-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fd3d-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fd3d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd3d-130">CommonParameters</span></span>
<span data-ttu-id="0fd3d-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd3d-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fd3d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd3d-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0fd3d-133">INPUTS</span></span>

### <span data-ttu-id="0fd3d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0fd3d-134">System.String</span></span>

### <span data-ttu-id="0fd3d-135">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0fd3d-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0fd3d-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0fd3d-136">OUTPUTS</span></span>

### <span data-ttu-id="0fd3d-137">System. Management. Automation. Runspaces. PSSession</span><span class="sxs-lookup"><span data-stu-id="0fd3d-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="0fd3d-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="0fd3d-138">NOTES</span></span>

## <span data-ttu-id="0fd3d-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0fd3d-139">RELATED LINKS</span></span>
