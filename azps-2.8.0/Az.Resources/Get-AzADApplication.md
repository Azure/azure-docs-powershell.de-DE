---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 18b5f64426b0a3c458ea489d27781f1a01336b52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825075"
---
# <span data-ttu-id="c76f9-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c76f9-101">Get-AzADApplication</span></span>

## <span data-ttu-id="c76f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c76f9-102">SYNOPSIS</span></span>
<span data-ttu-id="c76f9-103">Listet vorhandene Azure Active Directory-Anwendungen auf.</span><span class="sxs-lookup"><span data-stu-id="c76f9-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="c76f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c76f9-104">SYNTAX</span></span>

### <span data-ttu-id="c76f9-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c76f9-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c76f9-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c76f9-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c76f9-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c76f9-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c76f9-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c76f9-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c76f9-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c76f9-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c76f9-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="c76f9-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="c76f9-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c76f9-111">DESCRIPTION</span></span>
<span data-ttu-id="c76f9-112">Listet vorhandene Azure Active Directory-Anwendungen auf.</span><span class="sxs-lookup"><span data-stu-id="c76f9-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="c76f9-113">Die Anwendungssuche kann über ObjectID, ApplicationId, IdentifierUri oder DisplayName erfolgen.</span><span class="sxs-lookup"><span data-stu-id="c76f9-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="c76f9-114">Wenn kein Parameter angegeben wird, werden alle Anwendungen unter dem Mandanten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c76f9-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="c76f9-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c76f9-115">EXAMPLES</span></span>

### <span data-ttu-id="c76f9-116">Beispiel 1 – Auflisten aller Anwendungen</span><span class="sxs-lookup"><span data-stu-id="c76f9-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="c76f9-117">Listet alle Anwendungen unter einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="c76f9-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="c76f9-118">Beispiel für 2-Listen-Anwendungen mit Paging</span><span class="sxs-lookup"><span data-stu-id="c76f9-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="c76f9-119">Listet die ersten 100-Anwendungen unter einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="c76f9-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="c76f9-120">Beispiel 3: Abrufen der Anwendung nach Bezeichner-URI</span><span class="sxs-lookup"><span data-stu-id="c76f9-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="c76f9-121">Ruft die Anwendung mit dem Bezeichner-URI als " http://mySecretApp1 " ab.</span><span class="sxs-lookup"><span data-stu-id="c76f9-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="c76f9-122">Beispiel 4: Abrufen der Anwendung nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="c76f9-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="c76f9-123">Ruft die Anwendung mit der Objekt-ID "39e64ec6-569b-4030-8e1c-c3c519a05d69" ab.</span><span class="sxs-lookup"><span data-stu-id="c76f9-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="c76f9-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="c76f9-124">PARAMETERS</span></span>

### <span data-ttu-id="c76f9-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c76f9-125">-ApplicationId</span></span>
<span data-ttu-id="c76f9-126">Die Anwendungs-ID der Anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c76f9-126">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76f9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c76f9-127">-DefaultProfile</span></span>
<span data-ttu-id="c76f9-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c76f9-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c76f9-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c76f9-129">-DisplayName</span></span>
<span data-ttu-id="c76f9-130">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c76f9-130">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76f9-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="c76f9-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="c76f9-132">Ruft alle Anwendungen ab, beginnend mit dem Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="c76f9-132">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76f9-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="c76f9-133">-IdentifierUri</span></span>
<span data-ttu-id="c76f9-134">Eindeutiger Bezeichner-URI der Anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c76f9-134">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76f9-135">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c76f9-135">-ObjectId</span></span>
<span data-ttu-id="c76f9-136">Die Objekt-ID der abzurufenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c76f9-136">The object id of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76f9-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="c76f9-137">-IncludeTotalCount</span></span>
<span data-ttu-id="c76f9-138">Gibt die Anzahl der Objekte in der Datengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c76f9-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="c76f9-139">Derzeit hat dieser Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="c76f9-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="c76f9-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="c76f9-140">-Skip</span></span>
<span data-ttu-id="c76f9-141">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="c76f9-141">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76f9-142">-First</span><span class="sxs-lookup"><span data-stu-id="c76f9-142">-First</span></span>
<span data-ttu-id="c76f9-143">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c76f9-143">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76f9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c76f9-144">CommonParameters</span></span>
<span data-ttu-id="c76f9-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c76f9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c76f9-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c76f9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c76f9-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c76f9-147">INPUTS</span></span>

### <span data-ttu-id="c76f9-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c76f9-148">System.String</span></span>

### <span data-ttu-id="c76f9-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c76f9-149">System.Guid</span></span>

## <span data-ttu-id="c76f9-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c76f9-150">OUTPUTS</span></span>

### <span data-ttu-id="c76f9-151">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c76f9-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="c76f9-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="c76f9-152">NOTES</span></span>

## <span data-ttu-id="c76f9-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c76f9-153">RELATED LINKS</span></span>

[<span data-ttu-id="c76f9-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c76f9-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="c76f9-155">Neu – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c76f9-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="c76f9-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c76f9-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="c76f9-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c76f9-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="c76f9-158">Satz-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c76f9-158">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="c76f9-159">Neu – AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c76f9-159">New-AzADApplication</span></span>](./New-AzADApplication.md)

