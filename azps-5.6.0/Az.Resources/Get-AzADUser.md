---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 6f5ae29865775368427987dcfc1844c9235db593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923459"
---
# <span data-ttu-id="807a1-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="807a1-101">Get-AzADUser</span></span>

## <span data-ttu-id="807a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="807a1-102">SYNOPSIS</span></span>
<span data-ttu-id="807a1-103">Filtert Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="807a1-103">Filters active directory users.</span></span>

## <span data-ttu-id="807a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="807a1-104">SYNTAX</span></span>

### <span data-ttu-id="807a1-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="807a1-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="807a1-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="807a1-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="807a1-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="807a1-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="807a1-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="807a1-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="807a1-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="807a1-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="807a1-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="807a1-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="807a1-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="807a1-111">DESCRIPTION</span></span>
<span data-ttu-id="807a1-112">Filtert Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="807a1-112">Filters active directory users.</span></span>

## <span data-ttu-id="807a1-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="807a1-113">EXAMPLES</span></span>

### <span data-ttu-id="807a1-114">Beispiel 1: Auflisten aller Benutzer</span><span class="sxs-lookup"><span data-stu-id="807a1-114">Example 1: List all users</span></span>

```powershell
PS C:\> Get-AzADUser
```

<span data-ttu-id="807a1-115">Listet alle AD-Benutzer in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="807a1-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="807a1-116">Beispiel 2: Auflisten aller Benutzer mithilfe von Paging</span><span class="sxs-lookup"><span data-stu-id="807a1-116">Example 2: List all users using paging</span></span>

```powershell
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="807a1-117">Listet die ersten 100 AD-Benutzer in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="807a1-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="807a1-118">Beispiel 3: Anzeigen des Benutzers nach Dem Prinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="807a1-118">Example 3: Get AD user by user principal name</span></span>

```powershell
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="807a1-119">Ruft den AD-Benutzer mit dem Benutzernamen "" foo@domain.com ab.</span><span class="sxs-lookup"><span data-stu-id="807a1-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="807a1-120">Beispiel 4: Liste nach Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="807a1-120">Example 4: List by search string</span></span>

```powershell
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="807a1-121">Listet alle AD-Benutzer auf, deren Anzeigename mit "Joe" beginnt.</span><span class="sxs-lookup"><span data-stu-id="807a1-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="807a1-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="807a1-122">PARAMETERS</span></span>

### <span data-ttu-id="807a1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="807a1-123">-DefaultProfile</span></span>
<span data-ttu-id="807a1-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="807a1-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="807a1-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="807a1-125">-DisplayName</span></span>
<span data-ttu-id="807a1-126">Der Anzeigename des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="807a1-126">The display name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807a1-127">-Mail</span><span class="sxs-lookup"><span data-stu-id="807a1-127">-Mail</span></span>
<span data-ttu-id="807a1-128">Die E-Mail des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="807a1-128">The user mail.</span></span>

```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="807a1-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="807a1-129">-ObjectId</span></span>
<span data-ttu-id="807a1-130">Objekt-ID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="807a1-130">Object id of the user.</span></span>

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

### <span data-ttu-id="807a1-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="807a1-131">-StartsWith</span></span>
<span data-ttu-id="807a1-132">Wird verwendet, um Benutzer zu finden, die mit der bereitgestellten Zeichenfolge beginnen.</span><span class="sxs-lookup"><span data-stu-id="807a1-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="807a1-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="807a1-133">-UserPrincipalName</span></span>
<span data-ttu-id="807a1-134">UPN des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="807a1-134">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="807a1-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="807a1-135">-IncludeTotalCount</span></span>
<span data-ttu-id="807a1-136">Gibt die Anzahl der Objekte im Datensatz an.</span><span class="sxs-lookup"><span data-stu-id="807a1-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="807a1-137">Dieser Parameter führt zurzeit nichts aus.</span><span class="sxs-lookup"><span data-stu-id="807a1-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="807a1-138">-Skip</span><span class="sxs-lookup"><span data-stu-id="807a1-138">-Skip</span></span>
<span data-ttu-id="807a1-139">Ignoriert die ersten N-Objekte und ruft dann die verbleibenden Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="807a1-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="807a1-140">-First</span><span class="sxs-lookup"><span data-stu-id="807a1-140">-First</span></span>
<span data-ttu-id="807a1-141">Die maximale Anzahl von Zurücksennungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="807a1-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="807a1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="807a1-142">CommonParameters</span></span>
<span data-ttu-id="807a1-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="807a1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="807a1-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="807a1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="807a1-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="807a1-145">INPUTS</span></span>

### <span data-ttu-id="807a1-146">System.String</span><span class="sxs-lookup"><span data-stu-id="807a1-146">System.String</span></span>

## <span data-ttu-id="807a1-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="807a1-147">OUTPUTS</span></span>

### <span data-ttu-id="807a1-148">Microsoft.Azure.Commands.ActiveDirectory.PSDUser</span><span class="sxs-lookup"><span data-stu-id="807a1-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="807a1-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="807a1-149">NOTES</span></span>

## <span data-ttu-id="807a1-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="807a1-150">RELATED LINKS</span></span>

[<span data-ttu-id="807a1-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="807a1-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="807a1-152">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="807a1-152">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="807a1-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="807a1-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

