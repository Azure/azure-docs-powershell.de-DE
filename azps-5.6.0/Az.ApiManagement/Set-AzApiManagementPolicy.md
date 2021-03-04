---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: 3858d24bb0c714da0e48ad5834870ec5127eb5e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925288"
---
# <span data-ttu-id="a904c-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a904c-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="a904c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a904c-102">SYNOPSIS</span></span>
<span data-ttu-id="a904c-103">Legt die angegebene Bereichsrichtlinie für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="a904c-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="a904c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a904c-104">SYNTAX</span></span>

### <span data-ttu-id="a904c-105">SetTenantLevel (Standard)</span><span class="sxs-lookup"><span data-stu-id="a904c-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a904c-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="a904c-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a904c-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="a904c-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a904c-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="a904c-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a904c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a904c-109">DESCRIPTION</span></span>
<span data-ttu-id="a904c-110">Das **Cmdlet Set-AzApiManagementPolicy** legt die angegebene Bereichsrichtlinie für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="a904c-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="a904c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a904c-111">EXAMPLES</span></span>

### <span data-ttu-id="a904c-112">Beispiel 1: Festlegen der Richtlinie auf Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="a904c-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="a904c-113">Mit diesem Befehl wird die Richtlinie auf Mandantenebene aus einer Datei namens tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="a904c-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="a904c-114">Beispiel 2: Festlegen einer Richtlinie für den Produktbereich</span><span class="sxs-lookup"><span data-stu-id="a904c-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="a904c-115">Mit diesem Befehl wird die Richtlinie für den Produktbereich für die API-Verwaltung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a904c-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="a904c-116">Beispiel 3: Festlegen einer API-Bereichsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="a904c-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="a904c-117">Mit diesem Befehl wird die API-Scope-Richtlinie für die API-Verwaltung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a904c-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="a904c-118">Beispiel 4: Festlegen einer Vorgangsbereichsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="a904c-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="a904c-119">Mit diesem Befehl wird die Vorgangsbereichsrichtlinie für die API-Verwaltung definiert.</span><span class="sxs-lookup"><span data-stu-id="a904c-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="a904c-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a904c-120">PARAMETERS</span></span>

### <span data-ttu-id="a904c-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a904c-121">-ApiId</span></span>
<span data-ttu-id="a904c-122">Gibt den Bezeichner der vorhandenen API an.</span><span class="sxs-lookup"><span data-stu-id="a904c-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="a904c-123">Wenn Sie diesen Parameter angeben, legt das Cmdlet die RICHTLINIE für den API-Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="a904c-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a904c-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a904c-124">-ApiRevision</span></span>
<span data-ttu-id="a904c-125">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="a904c-125">Identifier of API Revision.</span></span> <span data-ttu-id="a904c-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a904c-126">This parameter is optional.</span></span> <span data-ttu-id="a904c-127">Wenn nicht angegeben, wird die Richtlinie in der aktuell aktiven Api-Überarbeitung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a904c-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a904c-128">-Context</span><span class="sxs-lookup"><span data-stu-id="a904c-128">-Context</span></span>
<span data-ttu-id="a904c-129">Gibt die Instanz von **PsApiManagementContext an.**</span><span class="sxs-lookup"><span data-stu-id="a904c-129">Specifies the instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a904c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a904c-130">-DefaultProfile</span></span>
<span data-ttu-id="a904c-131">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a904c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a904c-132">-Format</span><span class="sxs-lookup"><span data-stu-id="a904c-132">-Format</span></span>
<span data-ttu-id="a904c-133">Gibt das Format der Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="a904c-133">Specifies the format of the policy.</span></span> <span data-ttu-id="a904c-134">Wenn Sie `application/vnd.ms-azure-apim.policy+xml` verwenden, müssen in der Richtlinie enthaltene Ausdrücke xml-escaped sein.</span><span class="sxs-lookup"><span data-stu-id="a904c-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="a904c-135">Wenn sie `application/vnd.ms-azure-apim.policy.raw+xml` verwendet **wird, muss** die Richtlinie nicht als XML-Escape verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a904c-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="a904c-136">Der Standardwert ist `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="a904c-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="a904c-137">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a904c-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="a904c-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a904c-138">-OperationId</span></span>
<span data-ttu-id="a904c-139">Gibt den Bezeichner des vorhandenen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="a904c-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="a904c-140">Wenn mit ApiId angegeben wird, wird die Richtlinie für den Vorgangsbereich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a904c-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="a904c-141">Diese Parameter sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a904c-141">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a904c-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a904c-142">-PassThru</span></span>
<span data-ttu-id="a904c-143">passthru</span><span class="sxs-lookup"><span data-stu-id="a904c-143">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a904c-144">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a904c-144">-Policy</span></span>
<span data-ttu-id="a904c-145">Gibt das Richtliniendokument als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="a904c-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="a904c-146">Dieser Parameter ist erforderlich, wenn der -*PolicyFilePath* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a904c-146">This parameter is required if the -*PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="a904c-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="a904c-147">-PolicyFilePath</span></span>
<span data-ttu-id="a904c-148">Gibt den Dateipfad des Richtliniendokuments an.</span><span class="sxs-lookup"><span data-stu-id="a904c-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="a904c-149">Dieser Parameter ist erforderlich, wenn der *Parameter Richtlinie* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a904c-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="a904c-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="a904c-150">-PolicyUrl</span></span>
<span data-ttu-id="a904c-151">Die URL, in der das Richtliniendokument gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="a904c-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="a904c-152">Dieser Parameter ist erforderlich, wenn -Policy oder -PolicyFilePath nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a904c-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="a904c-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a904c-153">-ProductId</span></span>
<span data-ttu-id="a904c-154">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="a904c-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="a904c-155">Wenn dieser Parameter angegeben ist, legt das Cmdlet die Richtlinie für den Produktbereich fest.</span><span class="sxs-lookup"><span data-stu-id="a904c-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a904c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a904c-156">CommonParameters</span></span>
<span data-ttu-id="a904c-157">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a904c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a904c-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a904c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a904c-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a904c-159">INPUTS</span></span>

### <span data-ttu-id="a904c-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a904c-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a904c-161">System.String</span><span class="sxs-lookup"><span data-stu-id="a904c-161">System.String</span></span>

### <span data-ttu-id="a904c-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a904c-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a904c-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a904c-163">OUTPUTS</span></span>

### <span data-ttu-id="a904c-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a904c-164">System.Boolean</span></span>

## <span data-ttu-id="a904c-165">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a904c-165">NOTES</span></span>

## <span data-ttu-id="a904c-166">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a904c-166">RELATED LINKS</span></span>

[<span data-ttu-id="a904c-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a904c-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="a904c-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a904c-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


