---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 59bbe7c5309764c41f22aaa99dbb4d47a23f1ba8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843168"
---
# <span data-ttu-id="c1178-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c1178-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="c1178-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1178-102">SYNOPSIS</span></span>
<span data-ttu-id="c1178-103">Überprüft eine Ressourcengruppen Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c1178-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="c1178-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1178-104">SYNTAX</span></span>

### <span data-ttu-id="c1178-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1178-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1178-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c1178-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1178-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c1178-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1178-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c1178-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1178-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c1178-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1178-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c1178-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1178-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c1178-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1178-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c1178-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1178-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1178-113">DESCRIPTION</span></span>
<span data-ttu-id="c1178-114">Das Cmdlet **Test-AzResourceGroupDeployment** bestimmt, ob eine Azure Resource Group-Bereitstellungsvorlage und deren Parameterwerte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="c1178-114">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="c1178-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1178-115">EXAMPLES</span></span>

## <span data-ttu-id="c1178-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1178-116">PARAMETERS</span></span>

### <span data-ttu-id="c1178-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c1178-117">-ApiVersion</span></span>
<span data-ttu-id="c1178-118">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c1178-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c1178-119">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="c1178-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="c1178-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1178-120">-DefaultProfile</span></span>
<span data-ttu-id="c1178-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c1178-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1178-122">-Modus</span><span class="sxs-lookup"><span data-stu-id="c1178-122">-Mode</span></span>
<span data-ttu-id="c1178-123">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="c1178-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="c1178-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c1178-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c1178-125">Inkrementelle</span><span class="sxs-lookup"><span data-stu-id="c1178-125">Incremental</span></span>
- <span data-ttu-id="c1178-126">Komplette</span><span class="sxs-lookup"><span data-stu-id="c1178-126">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1178-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="c1178-127">-Pre</span></span>
<span data-ttu-id="c1178-128">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c1178-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c1178-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1178-129">-ResourceGroupName</span></span>
<span data-ttu-id="c1178-130">Gibt den Namen der zu testenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c1178-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="c1178-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="c1178-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="c1178-132">Rollback zur erfolgreichen Bereitstellung mit dem angegebenen Namen in der Ressourcengruppe sollte nicht verwendet werden, wenn-RollbackToLastDeployment verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1178-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1178-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="c1178-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="c1178-134">Rollback zur letzten erfolgreichen Bereitstellung in der Ressourcengruppe sollte nicht vorhanden sein, wenn-RollBackDeploymentName verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1178-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="c1178-135">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="c1178-135">-TemplateFile</span></span>
<span data-ttu-id="c1178-136">Gibt den vollständigen Pfad einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="c1178-136">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1178-137">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c1178-137">-TemplateParameterFile</span></span>
<span data-ttu-id="c1178-138">Gibt den vollständigen Pfad einer JSON-Datei an, die die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="c1178-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1178-139">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="c1178-139">-TemplateParameterObject</span></span>
<span data-ttu-id="c1178-140">Gibt eine Hashtabelle mit Vorlagenparameter Namen und-Werten an.</span><span class="sxs-lookup"><span data-stu-id="c1178-140">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1178-141">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="c1178-141">-TemplateParameterUri</span></span>
<span data-ttu-id="c1178-142">Gibt den URI einer Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="c1178-142">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1178-143">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c1178-143">-TemplateUri</span></span>
<span data-ttu-id="c1178-144">Gibt den URI einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="c1178-144">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1178-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1178-145">CommonParameters</span></span>
<span data-ttu-id="c1178-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1178-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1178-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1178-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1178-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1178-148">INPUTS</span></span>

### <span data-ttu-id="c1178-149">Keine</span><span class="sxs-lookup"><span data-stu-id="c1178-149">None</span></span>

## <span data-ttu-id="c1178-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1178-150">OUTPUTS</span></span>

### <span data-ttu-id="c1178-151">Microsoft. Azure. Commands. ResourceManager. Models. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="c1178-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="c1178-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1178-152">NOTES</span></span>

## <span data-ttu-id="c1178-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1178-153">RELATED LINKS</span></span>

[<span data-ttu-id="c1178-154">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c1178-154">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="c1178-155">Neu – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c1178-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="c1178-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c1178-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="c1178-157">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c1178-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


