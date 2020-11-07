---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 0dc49732a6e6ad614a0330c3fe24b412be898a54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823535"
---
# <span data-ttu-id="ab9cd-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ab9cd-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="ab9cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab9cd-102">SYNOPSIS</span></span>
<span data-ttu-id="ab9cd-103">Filtert Active Directory-Dienst Prinzipale.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="ab9cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab9cd-104">SYNTAX</span></span>

### <span data-ttu-id="ab9cd-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ab9cd-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ab9cd-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab9cd-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ab9cd-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab9cd-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ab9cd-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab9cd-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ab9cd-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab9cd-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ab9cd-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab9cd-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ab9cd-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab9cd-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="ab9cd-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab9cd-112">DESCRIPTION</span></span>
<span data-ttu-id="ab9cd-113">Filtert Active Directory-Dienst Prinzipale.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="ab9cd-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab9cd-114">EXAMPLES</span></span>

### <span data-ttu-id="ab9cd-115">Beispiel 1: Anzeigendienst Prinzipale einer Liste</span><span class="sxs-lookup"><span data-stu-id="ab9cd-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="ab9cd-116">Listet alle Anzeigendienst Prinzipale in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="ab9cd-117">Beispiel 2 – Auflisten von Anzeigendienst Prinzipalen mithilfe von Paging</span><span class="sxs-lookup"><span data-stu-id="ab9cd-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="ab9cd-118">Listet die ersten 100-Anzeigendienst Prinzipale in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="ab9cd-119">Beispiel für 3-Listen Dienst Prinzipale nach SPN</span><span class="sxs-lookup"><span data-stu-id="ab9cd-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="ab9cd-120">Listet Dienst Prinzipale mit dem SPN "36f81fc3-b00f-48cd-8218-3879f51ff39f" auf.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="ab9cd-121">Beispiel für 4-Listen Dienst Prinzipale nach Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ab9cd-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="ab9cd-122">Listet alle Anzeigendienst Prinzipale auf, deren Anzeigename mit "Web" beginnt.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="ab9cd-123">Beispiel 5-Listen Dienst Prinzipale durch Piping</span><span class="sxs-lookup"><span data-stu-id="ab9cd-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="ab9cd-124">Ruft die AD-Anwendung mit der Objekt-ID "39e64ec6-569b-4030-8e1c-c3c519a05d69" ab und leitet Sie an das Get-AzADServicePrincipal-Cmdlet weiter, um alle Dienst Prinzipale für diese Anwendung aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="ab9cd-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab9cd-125">PARAMETERS</span></span>

### <span data-ttu-id="ab9cd-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ab9cd-126">-ApplicationId</span></span>
<span data-ttu-id="ab9cd-127">Die Anwendungs-ID des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-127">The service principal application id.</span></span>

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

### <span data-ttu-id="ab9cd-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="ab9cd-128">-ApplicationObject</span></span>
<span data-ttu-id="ab9cd-129">Das Application-Objekt, dessen Dienstprinzipal abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab9cd-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab9cd-130">-DefaultProfile</span></span>
<span data-ttu-id="ab9cd-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ab9cd-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab9cd-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ab9cd-132">-DisplayName</span></span>
<span data-ttu-id="ab9cd-133">Der Anzeigename des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-133">The service principal display name.</span></span>

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

### <span data-ttu-id="ab9cd-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="ab9cd-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="ab9cd-135">Die Suchzeichenfolge des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-135">The service principal search string.</span></span>

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

### <span data-ttu-id="ab9cd-136">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="ab9cd-136">-ObjectId</span></span>
<span data-ttu-id="ab9cd-137">Objekt-ID des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-137">Object id of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab9cd-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ab9cd-138">-ServicePrincipalName</span></span>
<span data-ttu-id="ab9cd-139">SPN des Diensts.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-139">SPN of the service.</span></span>

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

### <span data-ttu-id="ab9cd-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="ab9cd-140">-IncludeTotalCount</span></span>
<span data-ttu-id="ab9cd-141">Gibt die Anzahl der Objekte in der Datengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="ab9cd-142">Derzeit hat dieser Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="ab9cd-143">-Skip</span><span class="sxs-lookup"><span data-stu-id="ab9cd-143">-Skip</span></span>
<span data-ttu-id="ab9cd-144">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="ab9cd-145">-First</span><span class="sxs-lookup"><span data-stu-id="ab9cd-145">-First</span></span>
<span data-ttu-id="ab9cd-146">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="ab9cd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab9cd-147">CommonParameters</span></span>
<span data-ttu-id="ab9cd-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab9cd-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab9cd-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab9cd-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab9cd-150">INPUTS</span></span>

### <span data-ttu-id="ab9cd-151">System. String</span><span class="sxs-lookup"><span data-stu-id="ab9cd-151">System.String</span></span>

### <span data-ttu-id="ab9cd-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ab9cd-152">System.Guid</span></span>

### <span data-ttu-id="ab9cd-153">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="ab9cd-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="ab9cd-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab9cd-154">OUTPUTS</span></span>

### <span data-ttu-id="ab9cd-155">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ab9cd-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="ab9cd-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab9cd-156">NOTES</span></span>

## <span data-ttu-id="ab9cd-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab9cd-157">RELATED LINKS</span></span>

[<span data-ttu-id="ab9cd-158">Neu – AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ab9cd-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="ab9cd-159">Satz-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ab9cd-159">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="ab9cd-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ab9cd-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="ab9cd-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ab9cd-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="ab9cd-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ab9cd-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

