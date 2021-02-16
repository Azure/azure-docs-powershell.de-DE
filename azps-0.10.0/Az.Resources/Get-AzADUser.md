---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: b5690dfc1d85483b10fc7cd08606c4555784e8e0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398732"
---
# <span data-ttu-id="f6aab-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="f6aab-101">Get-AzADUser</span></span>

## <span data-ttu-id="f6aab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6aab-102">SYNOPSIS</span></span>
<span data-ttu-id="f6aab-103">Filtert Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f6aab-103">Filters active directory users.</span></span>

## <span data-ttu-id="f6aab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6aab-104">SYNTAX</span></span>

### <span data-ttu-id="f6aab-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6aab-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f6aab-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6aab-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f6aab-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6aab-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f6aab-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6aab-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f6aab-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6aab-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f6aab-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6aab-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="f6aab-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6aab-111">DESCRIPTION</span></span>
<span data-ttu-id="f6aab-112">Filtert Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f6aab-112">Filters active directory users.</span></span>

## <span data-ttu-id="f6aab-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6aab-113">EXAMPLES</span></span>

### <span data-ttu-id="f6aab-114">Beispiel 1: Auflisten aller Benutzer</span><span class="sxs-lookup"><span data-stu-id="f6aab-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="f6aab-115">Listet alle Ad-Ad-Benutzer in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="f6aab-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="f6aab-116">Beispiel 2: Auflisten aller Benutzer mithilfe von Seiten</span><span class="sxs-lookup"><span data-stu-id="f6aab-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="f6aab-117">Listet die ersten 100 Ad-Benutzer in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="f6aab-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="f6aab-118">Beispiel 3: "Ad-Benutzer nach Benutzerprinzipalnamen erhalten"</span><span class="sxs-lookup"><span data-stu-id="f6aab-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="f6aab-119">Ruft den Ad-Benutzer mit dem Benutzerprinzipalnamen " foo@domain.com "" ab.</span><span class="sxs-lookup"><span data-stu-id="f6aab-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="f6aab-120">Beispiel 4: Auflisten nach Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f6aab-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="f6aab-121">Listet alle Ad-Benutzer auf, deren Anzeigename mit "Joe" beginnt.</span><span class="sxs-lookup"><span data-stu-id="f6aab-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="f6aab-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6aab-122">PARAMETERS</span></span>

### <span data-ttu-id="f6aab-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6aab-123">-DefaultProfile</span></span>
<span data-ttu-id="f6aab-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f6aab-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6aab-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f6aab-125">-DisplayName</span></span>
<span data-ttu-id="f6aab-126">Der Anzeigename des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f6aab-126">The display name of the user.</span></span>

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

### <span data-ttu-id="f6aab-127">-First</span><span class="sxs-lookup"><span data-stu-id="f6aab-127">-First</span></span>
<span data-ttu-id="f6aab-128">Die maximale Anzahl von Zurücksendungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="f6aab-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="f6aab-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="f6aab-129">-IncludeTotalCount</span></span>
<span data-ttu-id="f6aab-130">Meldet die Anzahl der Objekte im Datenset.</span><span class="sxs-lookup"><span data-stu-id="f6aab-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="f6aab-131">Derzeit führt dieser Parameter keine Anderen aus.</span><span class="sxs-lookup"><span data-stu-id="f6aab-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="f6aab-132">-Mail</span><span class="sxs-lookup"><span data-stu-id="f6aab-132">-Mail</span></span>
<span data-ttu-id="f6aab-133">Die E-Mail des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f6aab-133">The user mail.</span></span>

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

### <span data-ttu-id="f6aab-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f6aab-134">-ObjectId</span></span>
<span data-ttu-id="f6aab-135">Objekt-ID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f6aab-135">Object id of the user.</span></span>

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

### <span data-ttu-id="f6aab-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="f6aab-136">-Skip</span></span>
<span data-ttu-id="f6aab-137">Ignoriert die ersten N-Objekte und ruft dann die verbleibenden Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="f6aab-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="f6aab-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="f6aab-138">-StartsWith</span></span>
<span data-ttu-id="f6aab-139">Wird verwendet, um Benutzer zu finden, die mit der bereitgestellten Zeichenfolge beginnen.</span><span class="sxs-lookup"><span data-stu-id="f6aab-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="f6aab-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f6aab-140">-UserPrincipalName</span></span>
<span data-ttu-id="f6aab-141">UPN des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f6aab-141">UPN of the user.</span></span>

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

### <span data-ttu-id="f6aab-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6aab-142">CommonParameters</span></span>
<span data-ttu-id="f6aab-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6aab-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6aab-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6aab-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6aab-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6aab-145">INPUTS</span></span>

### <span data-ttu-id="f6aab-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f6aab-146">System.String</span></span>

### <span data-ttu-id="f6aab-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f6aab-147">System.Guid</span></span>

## <span data-ttu-id="f6aab-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6aab-148">OUTPUTS</span></span>

### <span data-ttu-id="f6aab-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.WERDENDUser</span><span class="sxs-lookup"><span data-stu-id="f6aab-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="f6aab-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f6aab-150">NOTES</span></span>

## <span data-ttu-id="f6aab-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f6aab-151">RELATED LINKS</span></span>

[<span data-ttu-id="f6aab-152">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="f6aab-152">New-AzADUser</span></span>](./New-AzADUser.md)


[<span data-ttu-id="f6aab-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="f6aab-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

