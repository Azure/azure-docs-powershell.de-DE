---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 01f6b6d6ed119945af7d99bac9227c788976cbab
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398698"
---
# <span data-ttu-id="7a6c8-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7a6c8-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="7a6c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a6c8-102">SYNOPSIS</span></span>
<span data-ttu-id="7a6c8-103">Filtert active Directory-Dienstprinzipale.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="7a6c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a6c8-104">SYNTAX</span></span>

### <span data-ttu-id="7a6c8-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a6c8-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7a6c8-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a6c8-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7a6c8-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a6c8-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7a6c8-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a6c8-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7a6c8-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a6c8-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7a6c8-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a6c8-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7a6c8-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a6c8-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="7a6c8-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a6c8-112">DESCRIPTION</span></span>
<span data-ttu-id="7a6c8-113">Filtert active Directory-Dienstprinzipale.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="7a6c8-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a6c8-114">EXAMPLES</span></span>

### <span data-ttu-id="7a6c8-115">Beispiel 1: Auflisten der Ad-Dienstprinzipale</span><span class="sxs-lookup"><span data-stu-id="7a6c8-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="7a6c8-116">Listet alle Prinzipale für ad-Dienste in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="7a6c8-117">Beispiel 2: Auflisten der Ad -Dienstprinzipale mithilfe von Seiten</span><span class="sxs-lookup"><span data-stu-id="7a6c8-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="7a6c8-118">Listet die ersten 100 Ad-Dienstprinzipale in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="7a6c8-119">Beispiel 3: Auflisten der Dienstprinzipale nach SPN</span><span class="sxs-lookup"><span data-stu-id="7a6c8-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="7a6c8-120">Listet Dienstprinzipale mit dem SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f' auf.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="7a6c8-121">Beispiel 4: Auflisten der Dienstprinzipale nach Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7a6c8-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="7a6c8-122">Listet alle Ad-Dienstprinzipale auf, deren Anzeigename mit "Web" beginnt.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="7a6c8-123">Beispiel 5: Auflisten der Dienstprinzipale durch Piping</span><span class="sxs-lookup"><span data-stu-id="7a6c8-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="7a6c8-124">Ruft die Get-AzADServicePrincipal mit der Objekt-ID '39e64ec6-569b-4030-8e1c-c3c519a05d69' ab und gibt sie an das Cmdlet Get-AzADServicePrincipal weiter, um alle Dienstprinzipale für diese Anwendung auflisten.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="7a6c8-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a6c8-125">PARAMETERS</span></span>

### <span data-ttu-id="7a6c8-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7a6c8-126">-ApplicationId</span></span>
<span data-ttu-id="7a6c8-127">Die Dienstprinzipalanwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-127">The service principal application id.</span></span>

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

### <span data-ttu-id="7a6c8-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="7a6c8-128">-ApplicationObject</span></span>
<span data-ttu-id="7a6c8-129">Das Anwendungsobjekt, dessen Dienstprinzipal abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a6c8-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a6c8-130">-DefaultProfile</span></span>
<span data-ttu-id="7a6c8-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7a6c8-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a6c8-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7a6c8-132">-DisplayName</span></span>
<span data-ttu-id="7a6c8-133">Der Anzeigename des Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-133">The service principal display name.</span></span>

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

### <span data-ttu-id="7a6c8-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="7a6c8-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="7a6c8-135">Die Suchzeichenfolge des Dienstprinzipaldiensts.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-135">The service principal search string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a6c8-136">-First</span><span class="sxs-lookup"><span data-stu-id="7a6c8-136">-First</span></span>
<span data-ttu-id="7a6c8-137">Die maximale Anzahl der zurückzukehrende Objekte.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="7a6c8-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="7a6c8-138">-IncludeTotalCount</span></span>
<span data-ttu-id="7a6c8-139">Meldet die Anzahl der Objekte im Datenset.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="7a6c8-140">Derzeit führt dieser Parameter keine Anderen aus.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="7a6c8-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7a6c8-141">-ObjectId</span></span>
<span data-ttu-id="7a6c8-142">Objekt-ID des Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-142">Object id of the service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a6c8-143">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7a6c8-143">-ServicePrincipalName</span></span>
<span data-ttu-id="7a6c8-144">SPN des Diensts.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-144">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a6c8-145">-Skip</span><span class="sxs-lookup"><span data-stu-id="7a6c8-145">-Skip</span></span>
<span data-ttu-id="7a6c8-146">Ignoriert die ersten N-Objekte und ruft dann die verbleibenden Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="7a6c8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a6c8-147">CommonParameters</span></span>
<span data-ttu-id="7a6c8-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a6c8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a6c8-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a6c8-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a6c8-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a6c8-150">INPUTS</span></span>

### <span data-ttu-id="7a6c8-151">System.String</span><span class="sxs-lookup"><span data-stu-id="7a6c8-151">System.String</span></span>

### <span data-ttu-id="7a6c8-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7a6c8-152">System.Guid</span></span>

### <span data-ttu-id="7a6c8-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.WERDENDApplication</span><span class="sxs-lookup"><span data-stu-id="7a6c8-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="7a6c8-154">Parameter: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7a6c8-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="7a6c8-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a6c8-155">OUTPUTS</span></span>

### <span data-ttu-id="7a6c8-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.WAHLDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7a6c8-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="7a6c8-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7a6c8-157">NOTES</span></span>

## <span data-ttu-id="7a6c8-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7a6c8-158">RELATED LINKS</span></span>

[<span data-ttu-id="7a6c8-159">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7a6c8-159">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)


[<span data-ttu-id="7a6c8-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7a6c8-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="7a6c8-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7a6c8-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="7a6c8-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7a6c8-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

