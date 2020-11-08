---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: 9069dd055fd3cccdbd1efe520fc560c385d15cc3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997284"
---
# <span data-ttu-id="ff3bc-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="ff3bc-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="ff3bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff3bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff3bc-103">Aktualisiert die Vererbung der Restiction-Konfiguration für den Hauptwebsite Zugriff auf die SCM-Website für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ff3bc-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="ff3bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff3bc-104">SYNTAX</span></span>

### <span data-ttu-id="ff3bc-105">InputValuesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff3bc-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff3bc-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff3bc-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff3bc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff3bc-107">DESCRIPTION</span></span>
<span data-ttu-id="ff3bc-108">Das Cmdlet **Update-AzWebAppAccessRestrictionConfig** aktualisiert die Zugriffs Beschränkungs Konfiguration für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ff3bc-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="ff3bc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff3bc-109">EXAMPLES</span></span>

### <span data-ttu-id="ff3bc-110">Beispiel 1: Aktualisieren einer Web App SCM-Website, um Zugriffseinschränkungen von der Hauptwebsite zu verwenden</span><span class="sxs-lookup"><span data-stu-id="ff3bc-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>
```
PS C:\>Set-AzWebAppAccessRestriction -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -ScmSiteUseMainSiteRestrictionConfig
```

<span data-ttu-id="ff3bc-111">Mit diesem Befehl wird eine Web-App mit dem Namen "ContosoSite" aktualisiert, die zur Ressourcengruppe Default-Web-westus gehört, um die Zugriffs Beschränkungs Konfiguration der Hauptwebsite auf der SCM-Website zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff3bc-111">This command updates a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS to use access restriction config of main site on the scm site.</span></span>

## <span data-ttu-id="ff3bc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff3bc-112">PARAMETERS</span></span>

### <span data-ttu-id="ff3bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff3bc-113">-DefaultProfile</span></span>
<span data-ttu-id="ff3bc-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ff3bc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff3bc-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ff3bc-115">-InputObject</span></span>
<span data-ttu-id="ff3bc-116">Das Konfigurationsobjekt für Zugriffseinschränkungen</span><span class="sxs-lookup"><span data-stu-id="ff3bc-116">The access restriction config object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3bc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ff3bc-117">-Name</span></span>
<span data-ttu-id="ff3bc-118">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="ff3bc-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3bc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff3bc-119">-PassThru</span></span>
<span data-ttu-id="ff3bc-120">Gibt das Config-Objekt für die Zugriffsbeschränkung zurück.</span><span class="sxs-lookup"><span data-stu-id="ff3bc-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="ff3bc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff3bc-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff3bc-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ff3bc-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3bc-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="ff3bc-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="ff3bc-124">Die SCM-Website erbt Regeln, die auf der Hauptwebsite festgesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="ff3bc-124">Scm site inherits rules set on Main site.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3bc-125">-Slotname</span><span class="sxs-lookup"><span data-stu-id="ff3bc-125">-SlotName</span></span>
<span data-ttu-id="ff3bc-126">Name des Bereitstellungs Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="ff3bc-126">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3bc-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ff3bc-127">-Confirm</span></span>
<span data-ttu-id="ff3bc-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ff3bc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff3bc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff3bc-129">-WhatIf</span></span>
<span data-ttu-id="ff3bc-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff3bc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff3bc-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff3bc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff3bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff3bc-132">CommonParameters</span></span>
<span data-ttu-id="ff3bc-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff3bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff3bc-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff3bc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff3bc-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff3bc-135">INPUTS</span></span>

### <span data-ttu-id="ff3bc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ff3bc-136">System.String</span></span>

### <span data-ttu-id="ff3bc-137">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="ff3bc-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ff3bc-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff3bc-138">OUTPUTS</span></span>

### <span data-ttu-id="ff3bc-139">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="ff3bc-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="ff3bc-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff3bc-140">NOTES</span></span>

## <span data-ttu-id="ff3bc-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff3bc-141">RELATED LINKS</span></span>

[<span data-ttu-id="ff3bc-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="ff3bc-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="ff3bc-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="ff3bc-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="ff3bc-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="ff3bc-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
