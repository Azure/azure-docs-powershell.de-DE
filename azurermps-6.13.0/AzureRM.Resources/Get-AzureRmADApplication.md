---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: d36bca60f722498beaa831c2a630b23d8a709019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495725"
---
# <span data-ttu-id="419d1-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="419d1-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="419d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="419d1-102">SYNOPSIS</span></span>
<span data-ttu-id="419d1-103">Listet vorhandene Azure Active Directory-Anwendungen auf.</span><span class="sxs-lookup"><span data-stu-id="419d1-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="419d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="419d1-104">SYNTAX</span></span>

### <span data-ttu-id="419d1-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="419d1-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="419d1-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="419d1-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="419d1-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="419d1-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="419d1-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="419d1-108">SearchStringParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="419d1-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="419d1-109">DisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="419d1-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="419d1-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="419d1-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="419d1-111">DESCRIPTION</span></span>
<span data-ttu-id="419d1-112">Listet vorhandene Azure Active Directory-Anwendungen auf.</span><span class="sxs-lookup"><span data-stu-id="419d1-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="419d1-113">Die Anwendungssuche kann über ObjectID, ApplicationId, IdentifierUri oder DisplayName erfolgen.</span><span class="sxs-lookup"><span data-stu-id="419d1-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="419d1-114">Wenn kein Parameter angegeben wird, werden alle Anwendungen unter dem Mandanten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="419d1-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="419d1-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="419d1-115">EXAMPLES</span></span>

### <span data-ttu-id="419d1-116">Beispiel 1 – Auflisten aller Anwendungen</span><span class="sxs-lookup"><span data-stu-id="419d1-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzureRmADApplication
```

<span data-ttu-id="419d1-117">Listet alle Anwendungen unter einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="419d1-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="419d1-118">Beispiel für 2-Listen-Anwendungen mit Paging</span><span class="sxs-lookup"><span data-stu-id="419d1-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzureRmADApplication -First 100
```

<span data-ttu-id="419d1-119">Listet die ersten 100-Anwendungen unter einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="419d1-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="419d1-120">Beispiel 3: Abrufen der Anwendung nach Bezeichner-URI</span><span class="sxs-lookup"><span data-stu-id="419d1-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="419d1-121">Ruft die Anwendung mit dem Bezeichner-URI als " http://mySecretApp1 " ab.</span><span class="sxs-lookup"><span data-stu-id="419d1-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="419d1-122">Beispiel 4: Abrufen der Anwendung nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="419d1-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="419d1-123">Ruft die Anwendung mit der Objekt-ID "39e64ec6-569b-4030-8e1c-c3c519a05d69" ab.</span><span class="sxs-lookup"><span data-stu-id="419d1-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="419d1-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="419d1-124">PARAMETERS</span></span>

### <span data-ttu-id="419d1-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="419d1-125">-ApplicationId</span></span>
<span data-ttu-id="419d1-126">Die Anwendungs-ID der Anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="419d1-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="419d1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="419d1-127">-DefaultProfile</span></span>
<span data-ttu-id="419d1-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="419d1-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="419d1-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="419d1-129">-DisplayName</span></span>
<span data-ttu-id="419d1-130">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="419d1-130">The display name of the application.</span></span>

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

### <span data-ttu-id="419d1-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="419d1-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="419d1-132">Ruft alle Anwendungen ab, beginnend mit dem Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="419d1-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="419d1-133">-First</span><span class="sxs-lookup"><span data-stu-id="419d1-133">-First</span></span>
<span data-ttu-id="419d1-134">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="419d1-134">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="419d1-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="419d1-135">-IdentifierUri</span></span>
<span data-ttu-id="419d1-136">Eindeutiger Bezeichner-URI der Anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="419d1-136">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="419d1-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="419d1-137">-IncludeTotalCount</span></span>
<span data-ttu-id="419d1-138">Gibt die Anzahl der Objekte in der Datengruppe an.</span><span class="sxs-lookup"><span data-stu-id="419d1-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="419d1-139">Derzeit hat dieser Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="419d1-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="419d1-140">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="419d1-140">-ObjectId</span></span>
<span data-ttu-id="419d1-141">Die Objekt-ID der abzurufenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="419d1-141">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="419d1-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="419d1-142">-Skip</span></span>
<span data-ttu-id="419d1-143">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="419d1-143">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="419d1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="419d1-144">CommonParameters</span></span>
<span data-ttu-id="419d1-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="419d1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="419d1-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="419d1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="419d1-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="419d1-147">INPUTS</span></span>

### <span data-ttu-id="419d1-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="419d1-148">System.Guid</span></span>

### <span data-ttu-id="419d1-149">System. String</span><span class="sxs-lookup"><span data-stu-id="419d1-149">System.String</span></span>

## <span data-ttu-id="419d1-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="419d1-150">OUTPUTS</span></span>

### <span data-ttu-id="419d1-151">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="419d1-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="419d1-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="419d1-152">NOTES</span></span>

## <span data-ttu-id="419d1-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="419d1-153">RELATED LINKS</span></span>

[<span data-ttu-id="419d1-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="419d1-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="419d1-155">Neu – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="419d1-155">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="419d1-156">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="419d1-156">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="419d1-157">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="419d1-157">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="419d1-158">Satz-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="419d1-158">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="419d1-159">Neu – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="419d1-159">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

