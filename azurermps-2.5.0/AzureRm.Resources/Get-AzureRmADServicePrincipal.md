---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 10d95102058c759f9b2641f233bd590364945c71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849047"
---
# <span data-ttu-id="4447a-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4447a-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="4447a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4447a-102">SYNOPSIS</span></span>
<span data-ttu-id="4447a-103">Filtert Active Directory-Dienst Prinzipale.</span><span class="sxs-lookup"><span data-stu-id="4447a-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4447a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4447a-104">SYNTAX</span></span>

### <span data-ttu-id="4447a-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4447a-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4447a-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4447a-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4447a-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4447a-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4447a-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4447a-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4447a-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4447a-109">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4447a-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4447a-110">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4447a-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="4447a-111">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="4447a-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4447a-112">DESCRIPTION</span></span>
<span data-ttu-id="4447a-113">Filtert Active Directory-Dienst Prinzipale.</span><span class="sxs-lookup"><span data-stu-id="4447a-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="4447a-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4447a-114">EXAMPLES</span></span>

### <span data-ttu-id="4447a-115">Beispiel 1: Anzeigendienst Prinzipale einer Liste</span><span class="sxs-lookup"><span data-stu-id="4447a-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="4447a-116">Listet alle Anzeigendienst Prinzipale in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="4447a-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="4447a-117">Beispiel 2 – Auflisten von Anzeigendienst Prinzipalen mithilfe von Paging</span><span class="sxs-lookup"><span data-stu-id="4447a-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -First 100
```

<span data-ttu-id="4447a-118">Listet die ersten 100-Anzeigendienst Prinzipale in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="4447a-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="4447a-119">Beispiel für 3-Listen Dienst Prinzipale nach SPN</span><span class="sxs-lookup"><span data-stu-id="4447a-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="4447a-120">Listet Dienst Prinzipale mit dem SPN "36f81fc3-b00f-48cd-8218-3879f51ff39f" auf.</span><span class="sxs-lookup"><span data-stu-id="4447a-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="4447a-121">Beispiel für 4-Listen Dienst Prinzipale nach Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4447a-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="4447a-122">Listet alle Anzeigendienst Prinzipale auf, deren Anzeigename mit "Web" beginnt.</span><span class="sxs-lookup"><span data-stu-id="4447a-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="4447a-123">Beispiel 5-Listen Dienst Prinzipale durch Piping</span><span class="sxs-lookup"><span data-stu-id="4447a-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzureRmADServicePrincipal
```

<span data-ttu-id="4447a-124">Ruft die AD-Anwendung mit der Objekt-ID "39e64ec6-569b-4030-8e1c-c3c519a05d69" ab und leitet Sie an das Get-AzureRmADServicePrincipal-Cmdlet weiter, um alle Dienst Prinzipale für diese Anwendung aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="4447a-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzureRmADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="4447a-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="4447a-125">PARAMETERS</span></span>

### <span data-ttu-id="4447a-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4447a-126">-ApplicationId</span></span>
<span data-ttu-id="4447a-127">Die Anwendungs-ID des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="4447a-127">The service principal application id.</span></span>

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

### <span data-ttu-id="4447a-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="4447a-128">-ApplicationObject</span></span>
<span data-ttu-id="4447a-129">Das Application-Objekt, dessen Dienstprinzipal abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4447a-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="4447a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4447a-130">-DefaultProfile</span></span>
<span data-ttu-id="4447a-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4447a-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4447a-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4447a-132">-DisplayName</span></span>
<span data-ttu-id="4447a-133">Der Anzeigename des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="4447a-133">The service principal display name.</span></span>

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

### <span data-ttu-id="4447a-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="4447a-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="4447a-135">Die Suchzeichenfolge des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="4447a-135">The service principal search string.</span></span>

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

### <span data-ttu-id="4447a-136">-First</span><span class="sxs-lookup"><span data-stu-id="4447a-136">-First</span></span>
<span data-ttu-id="4447a-137">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4447a-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="4447a-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="4447a-138">-IncludeTotalCount</span></span>
<span data-ttu-id="4447a-139">Gibt die Anzahl der Objekte in der Datengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4447a-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="4447a-140">Derzeit hat dieser Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="4447a-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="4447a-141">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="4447a-141">-ObjectId</span></span>
<span data-ttu-id="4447a-142">Objekt-ID des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="4447a-142">Object id of the service principal.</span></span>

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

### <span data-ttu-id="4447a-143">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="4447a-143">-ServicePrincipalName</span></span>
<span data-ttu-id="4447a-144">SPN des Diensts.</span><span class="sxs-lookup"><span data-stu-id="4447a-144">SPN of the service.</span></span>

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

### <span data-ttu-id="4447a-145">-Skip</span><span class="sxs-lookup"><span data-stu-id="4447a-145">-Skip</span></span>
<span data-ttu-id="4447a-146">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="4447a-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="4447a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4447a-147">CommonParameters</span></span>
<span data-ttu-id="4447a-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4447a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4447a-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4447a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4447a-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4447a-150">INPUTS</span></span>

### <span data-ttu-id="4447a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="4447a-151">System.String</span></span>

### <span data-ttu-id="4447a-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="4447a-152">System.Guid</span></span>

### <span data-ttu-id="4447a-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="4447a-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="4447a-154">Parameter: applicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4447a-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="4447a-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4447a-155">OUTPUTS</span></span>

### <span data-ttu-id="4447a-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4447a-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="4447a-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="4447a-157">NOTES</span></span>

## <span data-ttu-id="4447a-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4447a-158">RELATED LINKS</span></span>

[<span data-ttu-id="4447a-159">Neu – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4447a-159">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)



[<span data-ttu-id="4447a-160">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4447a-160">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="4447a-161">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4447a-161">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="4447a-162">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4447a-162">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

