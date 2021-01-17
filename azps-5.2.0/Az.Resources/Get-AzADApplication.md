---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 68344fcafa16187651615c95ec2fb41d0bbbfb82
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365908"
---
# <span data-ttu-id="d3929-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d3929-101">Get-AzADApplication</span></span>

## <span data-ttu-id="d3929-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3929-102">SYNOPSIS</span></span>
<span data-ttu-id="d3929-103">Listet vorhandene Azure Active Directory-Anwendungen auf.</span><span class="sxs-lookup"><span data-stu-id="d3929-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="d3929-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3929-104">SYNTAX</span></span>

### <span data-ttu-id="d3929-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3929-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d3929-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3929-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d3929-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3929-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d3929-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3929-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d3929-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3929-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d3929-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3929-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="d3929-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3929-111">DESCRIPTION</span></span>
<span data-ttu-id="d3929-112">Listet vorhandene Azure Active Directory-Anwendungen auf.</span><span class="sxs-lookup"><span data-stu-id="d3929-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="d3929-113">Die Anwendungs-Suche kann mit ObjectId, ApplicationId, IdentifierUri oder DisplayName durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d3929-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="d3929-114">Wenn kein Parameter angegeben wird, ruft er alle Anwendungen unter dem Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="d3929-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="d3929-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d3929-115">EXAMPLES</span></span>

### <span data-ttu-id="d3929-116">Beispiel 1: Auflisten aller Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d3929-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="d3929-117">Listet alle Anwendungen unter einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="d3929-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="d3929-118">Beispiel 2: Auflisten von Anwendungen mithilfe von Seitenumlagerungen</span><span class="sxs-lookup"><span data-stu-id="d3929-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="d3929-119">Listet die ersten 100 Anwendungen unter einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="d3929-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="d3929-120">Beispiel 3: "Anwendung nach Bezeichner-URI erhalten"</span><span class="sxs-lookup"><span data-stu-id="d3929-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="d3929-121">Ruft die Anwendung mit dem Bezeichner-URI als " http://mySecretApp1 " ab.</span><span class="sxs-lookup"><span data-stu-id="d3929-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="d3929-122">Beispiel 4: Anwendung nach Objekt-ID erhalten</span><span class="sxs-lookup"><span data-stu-id="d3929-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="d3929-123">Ruft die Anwendung mit der Objekt-ID '39e64ec6-569b-4030-8e1c-c3c519a05d69' ab.</span><span class="sxs-lookup"><span data-stu-id="d3929-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="d3929-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3929-124">PARAMETERS</span></span>

### <span data-ttu-id="d3929-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d3929-125">-ApplicationId</span></span>
<span data-ttu-id="d3929-126">Die Anwendungs-ID der anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3929-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="d3929-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3929-127">-DefaultProfile</span></span>
<span data-ttu-id="d3929-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d3929-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3929-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d3929-129">-DisplayName</span></span>
<span data-ttu-id="d3929-130">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d3929-130">The display name of the application.</span></span>

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

### <span data-ttu-id="d3929-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="d3929-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="d3929-132">Rufen Sie alle Anwendungen ab dem Anzeigenamen ab.</span><span class="sxs-lookup"><span data-stu-id="d3929-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="d3929-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="d3929-133">-IdentifierUri</span></span>
<span data-ttu-id="d3929-134">Eindeutiger Bezeichner-URI der anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3929-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="d3929-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d3929-135">-ObjectId</span></span>
<span data-ttu-id="d3929-136">Die Objekt-ID der anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3929-136">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="d3929-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="d3929-137">-IncludeTotalCount</span></span>
<span data-ttu-id="d3929-138">Meldet die Anzahl der Objekte im Datenset.</span><span class="sxs-lookup"><span data-stu-id="d3929-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="d3929-139">Derzeit führt dieser Parameter keine Anderen aus.</span><span class="sxs-lookup"><span data-stu-id="d3929-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="d3929-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="d3929-140">-Skip</span></span>
<span data-ttu-id="d3929-141">Ignoriert die ersten N-Objekte und ruft dann die verbleibenden Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="d3929-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="d3929-142">-First</span><span class="sxs-lookup"><span data-stu-id="d3929-142">-First</span></span>
<span data-ttu-id="d3929-143">Die maximale Anzahl von Zurücksendungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="d3929-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="d3929-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3929-144">CommonParameters</span></span>
<span data-ttu-id="d3929-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3929-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3929-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3929-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3929-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d3929-147">INPUTS</span></span>

### <span data-ttu-id="d3929-148">System.String</span><span class="sxs-lookup"><span data-stu-id="d3929-148">System.String</span></span>

### <span data-ttu-id="d3929-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d3929-149">System.Guid</span></span>

## <span data-ttu-id="d3929-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d3929-150">OUTPUTS</span></span>

### <span data-ttu-id="d3929-151">Microsoft.Azure.Commands.ActiveDirectory.WERDENDApplication</span><span class="sxs-lookup"><span data-stu-id="d3929-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="d3929-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d3929-152">NOTES</span></span>

## <span data-ttu-id="d3929-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d3929-153">RELATED LINKS</span></span>

[<span data-ttu-id="d3929-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d3929-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="d3929-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d3929-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="d3929-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d3929-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="d3929-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d3929-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="d3929-158">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d3929-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="d3929-159">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d3929-159">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

