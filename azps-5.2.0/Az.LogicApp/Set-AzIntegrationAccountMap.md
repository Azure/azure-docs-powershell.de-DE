---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: fd077d5648f831c0b7c0562c3d3bcb642bd639b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368400"
---
# <span data-ttu-id="c04a5-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c04a5-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="c04a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c04a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c04a5-103">Ändert eine Integrationskontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="c04a5-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="c04a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c04a5-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c04a5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c04a5-105">DESCRIPTION</span></span>
<span data-ttu-id="c04a5-106">Das **Cmdlet Set-AzIntegrationAccountMap** ändert eine Integrationskontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="c04a5-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="c04a5-107">Dieses Cmdlet gibt ein Objekt zurück, das die Zuordnung des Integrationskontos darstellt.</span><span class="sxs-lookup"><span data-stu-id="c04a5-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="c04a5-108">Geben Sie den Namen des Integrationskontos, den Ressourcengruppennamen und den Zuordnungsnamen an.</span><span class="sxs-lookup"><span data-stu-id="c04a5-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="c04a5-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="c04a5-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c04a5-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="c04a5-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c04a5-111">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="c04a5-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c04a5-112">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c04a5-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c04a5-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c04a5-113">EXAMPLES</span></span>

### <span data-ttu-id="c04a5-114">Beispiel 1: Ändern einer Zuordnung eines Integrationskontos</span><span class="sxs-lookup"><span data-stu-id="c04a5-114">Example 1: Modify an integration account map</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="c04a5-115">Mit diesem Befehl wird die Zuordnung des Integrationskontos in der angegebenen Ressourcengruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="c04a5-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="c04a5-116">Der Befehl gibt eine Zuordnungsdefinition an, die in der $MapContent durch einen vorherigen Befehl gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="c04a5-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="c04a5-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c04a5-117">Example 2</span></span>

<span data-ttu-id="c04a5-118">Ändert eine Integrationskontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="c04a5-118">Modifies an integration account map.</span></span> <span data-ttu-id="c04a5-119">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="c04a5-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="c04a5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c04a5-120">PARAMETERS</span></span>

### <span data-ttu-id="c04a5-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="c04a5-121">-ContentType</span></span>
<span data-ttu-id="c04a5-122">Gibt einen Inhaltstyp für die Integrationskontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="c04a5-122">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="c04a5-123">Dieses Cmdlet unterstützt Anwendung/XML als Karteninhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="c04a5-123">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="c04a5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c04a5-124">-DefaultProfile</span></span>
<span data-ttu-id="c04a5-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c04a5-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c04a5-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c04a5-126">-Force</span></span>
<span data-ttu-id="c04a5-127">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="c04a5-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c04a5-128">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="c04a5-128">-MapDefinition</span></span>
<span data-ttu-id="c04a5-129">Gibt ein Definitionsobjekt für die Zuordnung eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="c04a5-129">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="c04a5-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="c04a5-130">-MapFilePath</span></span>
<span data-ttu-id="c04a5-131">Gibt den Dateipfad einer Definition für die Zuordnung des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="c04a5-131">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="c04a5-132">-MapName</span><span class="sxs-lookup"><span data-stu-id="c04a5-132">-MapName</span></span>
<span data-ttu-id="c04a5-133">Gibt den Namen einer Integrationskontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="c04a5-133">Specifies the name of an integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c04a5-134">-MapType</span><span class="sxs-lookup"><span data-stu-id="c04a5-134">-MapType</span></span>
<span data-ttu-id="c04a5-135">Gibt den Typ für die Zuordnung des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="c04a5-135">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="c04a5-136">Dieses Cmdlet unterstützt Xslt als Kartentyp.</span><span class="sxs-lookup"><span data-stu-id="c04a5-136">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04a5-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c04a5-137">-Metadata</span></span>
<span data-ttu-id="c04a5-138">Gibt ein Metadatenobjekt für die Karte an.</span><span class="sxs-lookup"><span data-stu-id="c04a5-138">Specifies a metadata object for the map.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04a5-139">-Name</span><span class="sxs-lookup"><span data-stu-id="c04a5-139">-Name</span></span>
<span data-ttu-id="c04a5-140">Gibt den Namen des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="c04a5-140">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c04a5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c04a5-141">-ResourceGroupName</span></span>
<span data-ttu-id="c04a5-142">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c04a5-142">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c04a5-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c04a5-143">-Confirm</span></span>
<span data-ttu-id="c04a5-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c04a5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c04a5-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c04a5-145">-WhatIf</span></span>
<span data-ttu-id="c04a5-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c04a5-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c04a5-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c04a5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c04a5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c04a5-148">CommonParameters</span></span>
<span data-ttu-id="c04a5-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c04a5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c04a5-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c04a5-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c04a5-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c04a5-151">INPUTS</span></span>

### <span data-ttu-id="c04a5-152">System.String</span><span class="sxs-lookup"><span data-stu-id="c04a5-152">System.String</span></span>

## <span data-ttu-id="c04a5-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c04a5-153">OUTPUTS</span></span>

### <span data-ttu-id="c04a5-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c04a5-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="c04a5-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c04a5-155">NOTES</span></span>

## <span data-ttu-id="c04a5-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c04a5-156">RELATED LINKS</span></span>

[<span data-ttu-id="c04a5-157">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c04a5-157">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="c04a5-158">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c04a5-158">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="c04a5-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c04a5-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


