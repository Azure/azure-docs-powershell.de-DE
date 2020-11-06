---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 8073df3946f5bf42ee8b0e5f2c7ae7881e905eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498018"
---
# <span data-ttu-id="c7bed-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c7bed-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="c7bed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7bed-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bed-103">Legt die angegebene Bereichs Richtlinie für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="c7bed-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7bed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7bed-104">SYNTAX</span></span>

### <span data-ttu-id="c7bed-105">Mandantenebene (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7bed-105">Tenant level (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7bed-106">Produktebene</span><span class="sxs-lookup"><span data-stu-id="c7bed-106">Product level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7bed-107">API-Ebene</span><span class="sxs-lookup"><span data-stu-id="c7bed-107">API level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7bed-108">Vorgangsebene</span><span class="sxs-lookup"><span data-stu-id="c7bed-108">Operation level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7bed-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7bed-109">DESCRIPTION</span></span>
<span data-ttu-id="c7bed-110">Das Cmdlet " **Set-AzureRmApiManagementPolicy** " legt die angegebene Bereichs Richtlinie für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="c7bed-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="c7bed-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7bed-111">EXAMPLES</span></span>

### <span data-ttu-id="c7bed-112">Beispiel 1: Festlegen der Richtlinie für Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="c7bed-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="c7bed-113">Dieser Befehl legt die Richtlinie für Mandantenebene aus einer Datei mit dem Namen tenantpolicy.xml fest.</span><span class="sxs-lookup"><span data-stu-id="c7bed-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="c7bed-114">Beispiel 2: Festlegen einer Richtlinie für den Produktbereich</span><span class="sxs-lookup"><span data-stu-id="c7bed-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="c7bed-115">Dieser Befehl legt die Richtlinie für den Produktbereich für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="c7bed-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="c7bed-116">Beispiel 3: Festlegen von API-Bereichs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="c7bed-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="c7bed-117">Dieser Befehl legt API-Bereichs Richtlinien für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="c7bed-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="c7bed-118">Beispiel 4: Festlegen des Vorgangs Bereichs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="c7bed-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="c7bed-119">Dieser Befehl legt die Richtlinie für den Vorgangsbereich für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="c7bed-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="c7bed-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7bed-120">PARAMETERS</span></span>

### <span data-ttu-id="c7bed-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c7bed-121">-ApiId</span></span>
<span data-ttu-id="c7bed-122">Gibt den Bezeichner der vorhandenen API an.</span><span class="sxs-lookup"><span data-stu-id="c7bed-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="c7bed-123">Wenn Sie diesen Parameter angeben, legt das Cmdlet die Richtlinie für den API-Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="c7bed-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7bed-124">-Context</span><span class="sxs-lookup"><span data-stu-id="c7bed-124">-Context</span></span>
<span data-ttu-id="c7bed-125">Gibt die Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="c7bed-125">Specifies the instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7bed-126">-Format</span><span class="sxs-lookup"><span data-stu-id="c7bed-126">-Format</span></span>
<span data-ttu-id="c7bed-127">Gibt das Format der Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="c7bed-127">Specifies the format of the policy.</span></span>
<span data-ttu-id="c7bed-128">Der Standardwert ist "application/vnd. ms-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="c7bed-128">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="c7bed-129">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="c7bed-129">-OperationId</span></span>
<span data-ttu-id="c7bed-130">Gibt den Bezeichner des vorhandenen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="c7bed-130">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="c7bed-131">Wenn mit ApiId angegeben, wird die Richtlinie für den Vorgangsbereich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c7bed-131">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="c7bed-132">Diese Parameter sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c7bed-132">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7bed-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7bed-133">-PassThru</span></span>
<span data-ttu-id="c7bed-134">passthru</span><span class="sxs-lookup"><span data-stu-id="c7bed-134">passthru</span></span>

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

### <span data-ttu-id="c7bed-135">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="c7bed-135">-Policy</span></span>
<span data-ttu-id="c7bed-136">Gibt das Richtliniendokument als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="c7bed-136">Specifies the policy document as a string.</span></span>
<span data-ttu-id="c7bed-137">Dieser Parameter ist erforderlich, wenn die- *PolicyFilePath* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c7bed-137">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="c7bed-138">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="c7bed-138">-PolicyFilePath</span></span>
<span data-ttu-id="c7bed-139">Gibt den Pfad der Richtliniendokument Datei an.</span><span class="sxs-lookup"><span data-stu-id="c7bed-139">Specifies the policy document file path.</span></span>
<span data-ttu-id="c7bed-140">Dieser Parameter ist erforderlich, wenn der *Richtlinien* Parameter nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c7bed-140">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="c7bed-141">-ProductID</span><span class="sxs-lookup"><span data-stu-id="c7bed-141">-ProductId</span></span>
<span data-ttu-id="c7bed-142">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="c7bed-142">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="c7bed-143">Wenn dieser Parameter angegeben wird, legt das Cmdlet die Richtlinie für den Produktbereich fest.</span><span class="sxs-lookup"><span data-stu-id="c7bed-143">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7bed-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7bed-144">-DefaultProfile</span></span>
<span data-ttu-id="c7bed-145">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7bed-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7bed-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bed-146">CommonParameters</span></span>
<span data-ttu-id="c7bed-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7bed-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bed-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7bed-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bed-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7bed-149">INPUTS</span></span>

## <span data-ttu-id="c7bed-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7bed-150">OUTPUTS</span></span>

### <span data-ttu-id="c7bed-151">bool</span><span class="sxs-lookup"><span data-stu-id="c7bed-151">bool</span></span>

## <span data-ttu-id="c7bed-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7bed-152">NOTES</span></span>

## <span data-ttu-id="c7bed-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7bed-153">RELATED LINKS</span></span>

[<span data-ttu-id="c7bed-154">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c7bed-154">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="c7bed-155">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c7bed-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


