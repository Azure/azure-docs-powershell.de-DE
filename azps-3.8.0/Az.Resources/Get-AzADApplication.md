---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: afcb95eca70c005023bacc2b2d71d9fda54c9259
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996733"
---
# <span data-ttu-id="92504-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="92504-101">Get-AzADApplication</span></span>

## <span data-ttu-id="92504-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92504-102">SYNOPSIS</span></span>
<span data-ttu-id="92504-103">Listet vorhandene Azure Active Directory-Anwendungen auf.</span><span class="sxs-lookup"><span data-stu-id="92504-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="92504-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92504-104">SYNTAX</span></span>

### <span data-ttu-id="92504-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="92504-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="92504-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92504-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="92504-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92504-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="92504-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="92504-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="92504-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="92504-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="92504-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="92504-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="92504-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92504-111">DESCRIPTION</span></span>
<span data-ttu-id="92504-112">Listet vorhandene Azure Active Directory-Anwendungen auf.</span><span class="sxs-lookup"><span data-stu-id="92504-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="92504-113">Die Anwendungssuche kann über ObjectID, ApplicationId, IdentifierUri oder DisplayName erfolgen.</span><span class="sxs-lookup"><span data-stu-id="92504-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="92504-114">Wenn kein Parameter angegeben wird, werden alle Anwendungen unter dem Mandanten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="92504-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="92504-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92504-115">EXAMPLES</span></span>

### <span data-ttu-id="92504-116">Beispiel 1 – Auflisten aller Anwendungen</span><span class="sxs-lookup"><span data-stu-id="92504-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="92504-117">Listet alle Anwendungen unter einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="92504-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="92504-118">Beispiel für 2-Listen-Anwendungen mit Paging</span><span class="sxs-lookup"><span data-stu-id="92504-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="92504-119">Listet die ersten 100-Anwendungen unter einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="92504-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="92504-120">Beispiel 3: Abrufen der Anwendung nach Bezeichner-URI</span><span class="sxs-lookup"><span data-stu-id="92504-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="92504-121">Ruft die Anwendung mit dem Bezeichner-URI als " http://mySecretApp1 " ab.</span><span class="sxs-lookup"><span data-stu-id="92504-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="92504-122">Beispiel 4: Abrufen der Anwendung nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="92504-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="92504-123">Ruft die Anwendung mit der Objekt-ID "39e64ec6-569b-4030-8e1c-c3c519a05d69" ab.</span><span class="sxs-lookup"><span data-stu-id="92504-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="92504-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="92504-124">PARAMETERS</span></span>

### <span data-ttu-id="92504-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="92504-125">-ApplicationId</span></span>
<span data-ttu-id="92504-126">Die Anwendungs-ID der Anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="92504-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="92504-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92504-127">-DefaultProfile</span></span>
<span data-ttu-id="92504-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="92504-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92504-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="92504-129">-DisplayName</span></span>
<span data-ttu-id="92504-130">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="92504-130">The display name of the application.</span></span>

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

### <span data-ttu-id="92504-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="92504-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="92504-132">Ruft alle Anwendungen ab, beginnend mit dem Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="92504-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="92504-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="92504-133">-IdentifierUri</span></span>
<span data-ttu-id="92504-134">Eindeutiger Bezeichner-URI der Anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="92504-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="92504-135">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="92504-135">-ObjectId</span></span>
<span data-ttu-id="92504-136">Die Objekt-ID der abzurufenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="92504-136">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="92504-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="92504-137">-IncludeTotalCount</span></span>
<span data-ttu-id="92504-138">Gibt die Anzahl der Objekte in der Datengruppe an.</span><span class="sxs-lookup"><span data-stu-id="92504-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="92504-139">Derzeit hat dieser Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="92504-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="92504-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="92504-140">-Skip</span></span>
<span data-ttu-id="92504-141">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="92504-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="92504-142">-First</span><span class="sxs-lookup"><span data-stu-id="92504-142">-First</span></span>
<span data-ttu-id="92504-143">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="92504-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="92504-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92504-144">CommonParameters</span></span>
<span data-ttu-id="92504-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92504-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92504-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92504-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92504-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92504-147">INPUTS</span></span>

### <span data-ttu-id="92504-148">System. String</span><span class="sxs-lookup"><span data-stu-id="92504-148">System.String</span></span>

### <span data-ttu-id="92504-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="92504-149">System.Guid</span></span>

## <span data-ttu-id="92504-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92504-150">OUTPUTS</span></span>

### <span data-ttu-id="92504-151">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="92504-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="92504-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="92504-152">NOTES</span></span>

## <span data-ttu-id="92504-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92504-153">RELATED LINKS</span></span>

[<span data-ttu-id="92504-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="92504-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="92504-155">Neu – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="92504-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="92504-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="92504-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="92504-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="92504-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="92504-158">Satz-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="92504-158">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="92504-159">Neu – AzADApplication</span><span class="sxs-lookup"><span data-stu-id="92504-159">New-AzADApplication</span></span>](./New-AzADApplication.md)

