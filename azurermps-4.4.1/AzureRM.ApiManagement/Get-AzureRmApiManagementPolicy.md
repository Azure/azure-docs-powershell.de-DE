---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 16eed643397245fa54b2876430042335762ea048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498105"
---
# <span data-ttu-id="4e4d0-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4e4d0-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="4e4d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e4d0-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4d0-103">Ruft die angegebene Bereichs Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e4d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e4d0-104">SYNTAX</span></span>

### <span data-ttu-id="4e4d0-105">Mandantenebene (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e4d0-105">Tenant level (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e4d0-106">Produktebene</span><span class="sxs-lookup"><span data-stu-id="4e4d0-106">Product level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e4d0-107">API-Ebene</span><span class="sxs-lookup"><span data-stu-id="4e4d0-107">API level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e4d0-108">Vorgangsebene</span><span class="sxs-lookup"><span data-stu-id="4e4d0-108">Operation level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e4d0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e4d0-109">DESCRIPTION</span></span>
<span data-ttu-id="4e4d0-110">Das Cmdlet " **Get-AzureRmApiManagementPolicy** " Ruft die angegebene Bereichs Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="4e4d0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e4d0-111">EXAMPLES</span></span>

### <span data-ttu-id="4e4d0-112">Beispiel 1: Abrufen der Richtlinie für Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="4e4d0-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="4e4d0-113">Dieser Befehl ruft die Richtlinie für Mandantenebene ab und speichert Sie in einer Datei mit dem Namen tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="4e4d0-114">Beispiel 2: Abrufen der Richtlinie für den Produktbereich</span><span class="sxs-lookup"><span data-stu-id="4e4d0-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="4e4d0-115">Dieser Befehl ruft die Richtlinie für den Produktbereich ab</span><span class="sxs-lookup"><span data-stu-id="4e4d0-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="4e4d0-116">Beispiel 3: Abrufen der API-Bereichs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="4e4d0-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="4e4d0-117">Dieser Befehl ruft eine Richtlinie für den API-Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="4e4d0-118">Beispiel 4: Abrufen der Richtlinie für den Vorgangsbereich</span><span class="sxs-lookup"><span data-stu-id="4e4d0-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="4e4d0-119">Mit diesem Befehl wird die Richtlinie für den Vorgangsbereich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="4e4d0-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e4d0-120">PARAMETERS</span></span>

### <span data-ttu-id="4e4d0-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4e4d0-121">-ApiId</span></span>
<span data-ttu-id="4e4d0-122">Gibt den Bezeichner der vorhandenen API an.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="4e4d0-123">Wenn Sie diesen Parameter angeben, gibt das Cmdlet die Richtlinie für den API-Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

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

### <span data-ttu-id="4e4d0-124">-Context</span><span class="sxs-lookup"><span data-stu-id="4e4d0-124">-Context</span></span>
<span data-ttu-id="4e4d0-125">Gibt eine Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-125">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="4e4d0-126">-Force</span><span class="sxs-lookup"><span data-stu-id="4e4d0-126">-Force</span></span>
<span data-ttu-id="4e4d0-127">ps_force</span><span class="sxs-lookup"><span data-stu-id="4e4d0-127">ps_force</span></span>

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

### <span data-ttu-id="4e4d0-128">-Format</span><span class="sxs-lookup"><span data-stu-id="4e4d0-128">-Format</span></span>
<span data-ttu-id="4e4d0-129">Gibt das Format der API-Verwaltungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-129">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="4e4d0-130">Der Standardwert für diesen Parameter ist "application/vnd. ms-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="4e4d0-130">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="4e4d0-131">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="4e4d0-131">-OperationId</span></span>
<span data-ttu-id="4e4d0-132">Gibt den Bezeichner des vorhandenen API-Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-132">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="4e4d0-133">Wenn Sie diesen Parameter mit *ApiId* angeben, gibt das Cmdlet die Richtlinie für den Vorgangsbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-133">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

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

### <span data-ttu-id="4e4d0-134">-ProductID</span><span class="sxs-lookup"><span data-stu-id="4e4d0-134">-ProductId</span></span>
<span data-ttu-id="4e4d0-135">Gibt den Bezeichner eines vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-135">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="4e4d0-136">Wenn Sie diesen Parameter angeben, gibt das Cmdlet die Richtlinie für den Produktbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-136">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

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

### <span data-ttu-id="4e4d0-137">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="4e4d0-137">-SaveAs</span></span>
<span data-ttu-id="4e4d0-138">Gibt den Dateipfad an, in dem das Ergebnis gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-138">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="4e4d0-139">Wenn Sie diesen Parameter nicht angeben, wird das Ergebnis als Stich Pipeline durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-139">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="4e4d0-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4e4d0-140">-Confirm</span></span>
<span data-ttu-id="4e4d0-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e4d0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e4d0-142">-WhatIf</span></span>
<span data-ttu-id="4e4d0-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e4d0-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e4d0-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4d0-145">-DefaultProfile</span></span>
<span data-ttu-id="4e4d0-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e4d0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4d0-147">CommonParameters</span></span>
<span data-ttu-id="4e4d0-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e4d0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4d0-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e4d0-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4d0-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e4d0-150">INPUTS</span></span>

## <span data-ttu-id="4e4d0-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e4d0-151">OUTPUTS</span></span>

### <span data-ttu-id="4e4d0-152">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4e4d0-152">String</span></span>

## <span data-ttu-id="4e4d0-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e4d0-153">NOTES</span></span>

## <span data-ttu-id="4e4d0-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e4d0-154">RELATED LINKS</span></span>

[<span data-ttu-id="4e4d0-155">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4e4d0-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="4e4d0-156">Satz-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4e4d0-156">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


