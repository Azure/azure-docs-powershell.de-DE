---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302307"
---
# <span data-ttu-id="87a81-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="87a81-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="87a81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87a81-102">SYNOPSIS</span></span>
<span data-ttu-id="87a81-103">Aktualisiert die Vererbung der Restiction-Konfiguration für den Hauptwebsite Zugriff auf die SCM-Website für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="87a81-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="87a81-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87a81-104">SYNTAX</span></span>

### <span data-ttu-id="87a81-105">InputValuesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="87a81-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87a81-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87a81-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87a81-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87a81-107">DESCRIPTION</span></span>
<span data-ttu-id="87a81-108">Das Cmdlet **Update-AzWebAppAccessRestrictionConfig** aktualisiert die Zugriffs Beschränkungs Konfiguration für eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="87a81-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="87a81-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87a81-109">EXAMPLES</span></span>

### <span data-ttu-id="87a81-110">Beispiel 1: Aktualisieren einer Web App SCM-Website, um Zugriffseinschränkungen von der Hauptwebsite zu verwenden</span><span class="sxs-lookup"><span data-stu-id="87a81-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="87a81-111">Im folgenden Beispiel wird eine Web-App mit dem Namen "IpRule" aktualisiert, die zur Ressourcengruppe myresourcegroup gehört, um die Zugriffs Beschränkungs Konfiguration der Hauptwebsite auf der SCM-Website zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="87a81-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="87a81-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="87a81-112">PARAMETERS</span></span>

### <span data-ttu-id="87a81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a81-113">-DefaultProfile</span></span>
<span data-ttu-id="87a81-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87a81-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87a81-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="87a81-115">-InputObject</span></span>
<span data-ttu-id="87a81-116">Das Konfigurationsobjekt für Zugriffseinschränkungen</span><span class="sxs-lookup"><span data-stu-id="87a81-116">The access restriction config object</span></span>

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

### <span data-ttu-id="87a81-117">-Name</span><span class="sxs-lookup"><span data-stu-id="87a81-117">-Name</span></span>
<span data-ttu-id="87a81-118">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="87a81-118">WebApp Name</span></span>

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

### <span data-ttu-id="87a81-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87a81-119">-PassThru</span></span>
<span data-ttu-id="87a81-120">Gibt das Config-Objekt für die Zugriffsbeschränkung zurück.</span><span class="sxs-lookup"><span data-stu-id="87a81-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="87a81-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87a81-121">-ResourceGroupName</span></span>
<span data-ttu-id="87a81-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="87a81-122">Resource Group Name</span></span>

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

### <span data-ttu-id="87a81-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="87a81-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="87a81-124">Die SCM-Website erbt Regeln, die auf der Hauptwebsite festgesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="87a81-124">Scm site inherits rules set on Main site.</span></span>

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

### <span data-ttu-id="87a81-125">-Slotname</span><span class="sxs-lookup"><span data-stu-id="87a81-125">-SlotName</span></span>
<span data-ttu-id="87a81-126">Name des Bereitstellungs Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="87a81-126">Deployment Slot name.</span></span>

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

### <span data-ttu-id="87a81-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87a81-127">-Confirm</span></span>
<span data-ttu-id="87a81-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87a81-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87a81-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87a81-129">-WhatIf</span></span>
<span data-ttu-id="87a81-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87a81-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87a81-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87a81-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87a81-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a81-132">CommonParameters</span></span>
<span data-ttu-id="87a81-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a81-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a81-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87a81-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a81-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87a81-135">INPUTS</span></span>

### <span data-ttu-id="87a81-136">System. String</span><span class="sxs-lookup"><span data-stu-id="87a81-136">System.String</span></span>

### <span data-ttu-id="87a81-137">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="87a81-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="87a81-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87a81-138">OUTPUTS</span></span>

### <span data-ttu-id="87a81-139">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="87a81-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="87a81-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="87a81-140">NOTES</span></span>

## <span data-ttu-id="87a81-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87a81-141">RELATED LINKS</span></span>

[<span data-ttu-id="87a81-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="87a81-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="87a81-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="87a81-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="87a81-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="87a81-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
