---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 97fbda90b27cbfabca8cbfd21c5bf375b86f7adb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849452"
---
# <span data-ttu-id="f8272-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f8272-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="f8272-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8272-102">SYNOPSIS</span></span>
<span data-ttu-id="f8272-103">Überprüft eine Ressourcengruppen Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="f8272-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8272-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8272-104">SYNTAX</span></span>

### <span data-ttu-id="f8272-105">ByTemplateFileWithNoParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8272-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8272-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f8272-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8272-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f8272-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8272-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f8272-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8272-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f8272-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8272-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f8272-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8272-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f8272-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8272-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f8272-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8272-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8272-113">DESCRIPTION</span></span>
<span data-ttu-id="f8272-114">Das Cmdlet **Test-AzureRmResourceGroupDeployment** bestimmt, ob eine Azure Resource Group-Bereitstellungsvorlage und deren Parameterwerte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="f8272-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="f8272-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8272-115">EXAMPLES</span></span>

## <span data-ttu-id="f8272-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8272-116">PARAMETERS</span></span>

### <span data-ttu-id="f8272-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f8272-117">-ApiVersion</span></span>
<span data-ttu-id="f8272-118">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f8272-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f8272-119">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="f8272-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f8272-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8272-120">-DefaultProfile</span></span>
<span data-ttu-id="f8272-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f8272-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8272-122">-Modus</span><span class="sxs-lookup"><span data-stu-id="f8272-122">-Mode</span></span>
<span data-ttu-id="f8272-123">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="f8272-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="f8272-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f8272-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f8272-125">Inkrementelle</span><span class="sxs-lookup"><span data-stu-id="f8272-125">Incremental</span></span>
- <span data-ttu-id="f8272-126">Komplette</span><span class="sxs-lookup"><span data-stu-id="f8272-126">Complete</span></span>

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

### <span data-ttu-id="f8272-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="f8272-127">-Pre</span></span>
<span data-ttu-id="f8272-128">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f8272-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f8272-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8272-129">-ResourceGroupName</span></span>
<span data-ttu-id="f8272-130">Gibt den Namen der zu testenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f8272-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="f8272-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="f8272-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="f8272-132">Rollback zur erfolgreichen Bereitstellung mit dem angegebenen Namen in der Ressourcengruppe sollte nicht verwendet werden, wenn-RollbackToLastDeployment verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f8272-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="f8272-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="f8272-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="f8272-134">Rollback zur letzten erfolgreichen Bereitstellung in der Ressourcengruppe sollte nicht vorhanden sein, wenn-RollBackDeploymentName verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f8272-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="f8272-135">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="f8272-135">-TemplateFile</span></span>
<span data-ttu-id="f8272-136">Gibt den vollständigen Pfad einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="f8272-136">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="f8272-137">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f8272-137">-TemplateParameterFile</span></span>
<span data-ttu-id="f8272-138">Gibt den vollständigen Pfad einer JSON-Datei an, die die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="f8272-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="f8272-139">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f8272-139">-TemplateParameterObject</span></span>
<span data-ttu-id="f8272-140">Gibt eine Hashtabelle mit Vorlagenparameter Namen und-Werten an.</span><span class="sxs-lookup"><span data-stu-id="f8272-140">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="f8272-141">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f8272-141">-TemplateParameterUri</span></span>
<span data-ttu-id="f8272-142">Gibt den URI einer Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="f8272-142">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="f8272-143">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f8272-143">-TemplateUri</span></span>
<span data-ttu-id="f8272-144">Gibt den URI einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="f8272-144">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="f8272-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8272-145">CommonParameters</span></span>
<span data-ttu-id="f8272-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8272-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8272-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8272-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8272-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8272-148">INPUTS</span></span>

### <span data-ttu-id="f8272-149">Keine</span><span class="sxs-lookup"><span data-stu-id="f8272-149">None</span></span>

## <span data-ttu-id="f8272-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8272-150">OUTPUTS</span></span>

### <span data-ttu-id="f8272-151">Microsoft. Azure. Commands. ResourceManager. Models. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="f8272-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="f8272-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8272-152">NOTES</span></span>

## <span data-ttu-id="f8272-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8272-153">RELATED LINKS</span></span>

[<span data-ttu-id="f8272-154">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f8272-154">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f8272-155">Neu – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f8272-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f8272-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f8272-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f8272-157">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f8272-157">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


