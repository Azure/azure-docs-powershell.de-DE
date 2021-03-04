---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 759977fb861f0ff2f1ede1fb28af50448b5ba5ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934707"
---
# <span data-ttu-id="1716a-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1716a-101">Get-AzADApplication</span></span>

## <span data-ttu-id="1716a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1716a-102">SYNOPSIS</span></span>
<span data-ttu-id="1716a-103">Listet vorhandene Azure Active Directory-Anwendungen auf.</span><span class="sxs-lookup"><span data-stu-id="1716a-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="1716a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1716a-104">SYNTAX</span></span>

### <span data-ttu-id="1716a-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1716a-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1716a-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1716a-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1716a-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1716a-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1716a-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1716a-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1716a-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1716a-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1716a-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="1716a-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="1716a-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1716a-111">DESCRIPTION</span></span>
<span data-ttu-id="1716a-112">Listet vorhandene Azure Active Directory-Anwendungen auf.</span><span class="sxs-lookup"><span data-stu-id="1716a-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="1716a-113">Das Anwendungssupup kann von ObjectId, ApplicationId, IdentifierUri oder DisplayName durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1716a-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="1716a-114">Wenn kein Parameter bereitgestellt wird, ruft er alle Anwendungen unter dem Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="1716a-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="1716a-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1716a-115">EXAMPLES</span></span>

### <span data-ttu-id="1716a-116">Beispiel 1 : Auflisten aller Anwendungen</span><span class="sxs-lookup"><span data-stu-id="1716a-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="1716a-117">Listet alle Anwendungen unter einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="1716a-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="1716a-118">Beispiel 2: Auflisten von Anwendungen mithilfe von Paging</span><span class="sxs-lookup"><span data-stu-id="1716a-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="1716a-119">Listet die ersten 100 Anwendungen unter einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="1716a-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="1716a-120">Beispiel 3 : URI "Anwendung nach Bezeichner" erhalten</span><span class="sxs-lookup"><span data-stu-id="1716a-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="1716a-121">Ruft die Anwendung mit bezeichner-uri als " http://mySecretApp1 ab.</span><span class="sxs-lookup"><span data-stu-id="1716a-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="1716a-122">Beispiel 4 : Anwendung nach Objekt-ID erhalten</span><span class="sxs-lookup"><span data-stu-id="1716a-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="1716a-123">Ruft die Anwendung mit der Objekt-ID '39e64ec6-569b-4030-8e1c-c3c519a05d69' ab.</span><span class="sxs-lookup"><span data-stu-id="1716a-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="1716a-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1716a-124">PARAMETERS</span></span>

### <span data-ttu-id="1716a-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1716a-125">-ApplicationId</span></span>
<span data-ttu-id="1716a-126">Die Anwendungs-ID der anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1716a-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="1716a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1716a-127">-DefaultProfile</span></span>
<span data-ttu-id="1716a-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1716a-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1716a-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1716a-129">-DisplayName</span></span>
<span data-ttu-id="1716a-130">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1716a-130">The display name of the application.</span></span>

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

### <span data-ttu-id="1716a-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="1716a-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="1716a-132">Rufen Sie alle Anwendungen ab dem Anzeigenamen ab.</span><span class="sxs-lookup"><span data-stu-id="1716a-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="1716a-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="1716a-133">-IdentifierUri</span></span>
<span data-ttu-id="1716a-134">Eindeutiger Bezeichner-Uri der anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1716a-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="1716a-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1716a-135">-ObjectId</span></span>
<span data-ttu-id="1716a-136">Die Objekt-ID der anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1716a-136">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="1716a-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="1716a-137">-IncludeTotalCount</span></span>
<span data-ttu-id="1716a-138">Gibt die Anzahl der Objekte im Datensatz an.</span><span class="sxs-lookup"><span data-stu-id="1716a-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="1716a-139">Dieser Parameter führt zurzeit nichts aus.</span><span class="sxs-lookup"><span data-stu-id="1716a-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="1716a-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="1716a-140">-Skip</span></span>
<span data-ttu-id="1716a-141">Ignoriert die ersten N-Objekte und ruft dann die verbleibenden Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="1716a-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="1716a-142">-First</span><span class="sxs-lookup"><span data-stu-id="1716a-142">-First</span></span>
<span data-ttu-id="1716a-143">Die maximale Anzahl von Zurücksennungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="1716a-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="1716a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1716a-144">CommonParameters</span></span>
<span data-ttu-id="1716a-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1716a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1716a-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1716a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1716a-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1716a-147">INPUTS</span></span>

### <span data-ttu-id="1716a-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1716a-148">System.String</span></span>

### <span data-ttu-id="1716a-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1716a-149">System.Guid</span></span>

## <span data-ttu-id="1716a-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1716a-150">OUTPUTS</span></span>

### <span data-ttu-id="1716a-151">Microsoft.Azure.Commands.ActiveDirectory.PSDApplication</span><span class="sxs-lookup"><span data-stu-id="1716a-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="1716a-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1716a-152">NOTES</span></span>

## <span data-ttu-id="1716a-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1716a-153">RELATED LINKS</span></span>

[<span data-ttu-id="1716a-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1716a-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="1716a-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1716a-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="1716a-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1716a-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="1716a-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1716a-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="1716a-158">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1716a-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="1716a-159">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1716a-159">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

