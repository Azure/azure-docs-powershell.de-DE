---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0631492bf2574fed7a9bb755088d811483504763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827203"
---
# <span data-ttu-id="1f773-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="1f773-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="1f773-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f773-102">SYNOPSIS</span></span>
<span data-ttu-id="1f773-103">Entfernt eine Zugriffs Einschränkungs Regel aus einer Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1f773-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="1f773-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f773-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-TargetScmSite] [-SlotName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f773-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f773-105">DESCRIPTION</span></span>
<span data-ttu-id="1f773-106">Das Cmdlet " **Remove-AzWebAppAccessRestrictionRule** " entfernt eine Zugriffs Einschränkungs Regel aus einer Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1f773-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="1f773-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f773-107">EXAMPLES</span></span>

### <span data-ttu-id="1f773-108">Beispiel 1: Entfernen einer Einschränkungs Regel für eine Web App-Zugriffsbeschränkung</span><span class="sxs-lookup"><span data-stu-id="1f773-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="1f773-109">Mit diesem Befehl wird die IpRule-Zugriffs Einschränkungs Regel aus Azure Web App mit dem Namen ContosoSite entfernt, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="1f773-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="1f773-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f773-110">PARAMETERS</span></span>

### <span data-ttu-id="1f773-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f773-111">-DefaultProfile</span></span>
<span data-ttu-id="1f773-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f773-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f773-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1f773-113">-Name</span></span>
<span data-ttu-id="1f773-114">Name der Zugriffs Beschränkungsregel</span><span class="sxs-lookup"><span data-stu-id="1f773-114">Access Restriction Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f773-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f773-115">-PassThru</span></span>
<span data-ttu-id="1f773-116">Gibt das Config-Objekt für die Zugriffsbeschränkung zurück.</span><span class="sxs-lookup"><span data-stu-id="1f773-116">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="1f773-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f773-117">-ResourceGroupName</span></span>
<span data-ttu-id="1f773-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="1f773-118">Resource Group Name</span></span>

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

### <span data-ttu-id="1f773-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="1f773-119">-SlotName</span></span>
<span data-ttu-id="1f773-120">Name des Bereitstellungs Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="1f773-120">Deployment Slot Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f773-121">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="1f773-121">-TargetScmSite</span></span>
<span data-ttu-id="1f773-122">Regel richtet sich an die Hauptwebsite oder die SCM-Website.</span><span class="sxs-lookup"><span data-stu-id="1f773-122">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="1f773-123">-Webbasierter</span><span class="sxs-lookup"><span data-stu-id="1f773-123">-WebAppName</span></span>
<span data-ttu-id="1f773-124">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="1f773-124">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f773-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f773-125">-Confirm</span></span>
<span data-ttu-id="1f773-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f773-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f773-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f773-127">-WhatIf</span></span>
<span data-ttu-id="1f773-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f773-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f773-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f773-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f773-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f773-130">CommonParameters</span></span>
<span data-ttu-id="1f773-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f773-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f773-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f773-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f773-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f773-133">INPUTS</span></span>

### <span data-ttu-id="1f773-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1f773-134">System.String</span></span>

## <span data-ttu-id="1f773-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f773-135">OUTPUTS</span></span>

### <span data-ttu-id="1f773-136">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="1f773-136">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="1f773-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f773-137">NOTES</span></span>

## <span data-ttu-id="1f773-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f773-138">RELATED LINKS</span></span>

[<span data-ttu-id="1f773-139">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="1f773-139">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="1f773-140">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="1f773-140">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="1f773-141">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="1f773-141">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
