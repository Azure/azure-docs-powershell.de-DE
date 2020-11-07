---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 40543468145c7fcfaf49fcfc7cad1cbf70938adf
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843471"
---
# <span data-ttu-id="b7c1c-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b7c1c-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="b7c1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c1c-103">Ruft eine Liste mit Anmeldeinformationen ab, die einem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b7c1c-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="b7c1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7c1c-104">SYNTAX</span></span>

### <span data-ttu-id="b7c1c-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b7c1c-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7c1c-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7c1c-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7c1c-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7c1c-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7c1c-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7c1c-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7c1c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7c1c-109">DESCRIPTION</span></span>
<span data-ttu-id="b7c1c-110">Mithilfe des Get-AzADSpCredential-Cmdlets können Sie eine Liste mit Anmeldeinformationen abrufen, die einem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b7c1c-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="b7c1c-111">Dieser Befehl ruft alle Anmelde Informationseigenschaften (aber nicht den Anmelde Informationswert) ab, die dem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b7c1c-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="b7c1c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7c1c-112">EXAMPLES</span></span>

### <span data-ttu-id="b7c1c-113">Beispiel 1 – Listen Anmeldeinformationen nach SPN</span><span class="sxs-lookup"><span data-stu-id="b7c1c-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="b7c1c-114">Gibt eine Liste der Anmeldeinformationen zurück, die dem Dienstprinzipal mit SPN ' ' zugeordnet sind http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="b7c1c-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="b7c1c-115">Beispiel 2: Auflisten von Anmeldeinformationen nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="b7c1c-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="b7c1c-116">Gibt eine Liste der Anmeldeinformationen zurück, die dem Dienstprinzipal mit der Objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b7c1c-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="b7c1c-117">Beispiel für 3-Listen-Anmeldeinformationen durch Piping</span><span class="sxs-lookup"><span data-stu-id="b7c1c-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="b7c1c-118">Ruft den Dienstprinzipal mit der Objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" ab und leitet ihn an das Get-AzADSpCredential-Cmdlet weiter, um alle Anmeldeinformationen für diesen Dienstprinzipal aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="b7c1c-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="b7c1c-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7c1c-119">PARAMETERS</span></span>

### <span data-ttu-id="b7c1c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c1c-120">-DefaultProfile</span></span>
<span data-ttu-id="b7c1c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b7c1c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7c1c-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b7c1c-122">-DisplayName</span></span>
<span data-ttu-id="b7c1c-123">Der Anzeigename des Dienst Prinzipals</span><span class="sxs-lookup"><span data-stu-id="b7c1c-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="b7c1c-124">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="b7c1c-124">-ObjectId</span></span>
<span data-ttu-id="b7c1c-125">Die Objekt-ID des Dienst Prinzipals, von dem die Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b7c1c-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c1c-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b7c1c-126">-ServicePrincipalName</span></span>
<span data-ttu-id="b7c1c-127">Der Name (SPN) des Dienst Prinzipals, aus dem Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b7c1c-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c1c-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="b7c1c-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="b7c1c-129">Das Dienstprinzipal Objekt, aus dem die Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b7c1c-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c1c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c1c-130">CommonParameters</span></span>
<span data-ttu-id="b7c1c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c1c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c1c-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c1c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c1c-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7c1c-133">INPUTS</span></span>

### <span data-ttu-id="b7c1c-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b7c1c-134">System.Guid</span></span>

### <span data-ttu-id="b7c1c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c1c-135">System.String</span></span>

### <span data-ttu-id="b7c1c-136">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b7c1c-136">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="b7c1c-137">Parameter: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b7c1c-137">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="b7c1c-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7c1c-138">OUTPUTS</span></span>

### <span data-ttu-id="b7c1c-139">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="b7c1c-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="b7c1c-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7c1c-140">NOTES</span></span>

## <span data-ttu-id="b7c1c-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7c1c-141">RELATED LINKS</span></span>

[<span data-ttu-id="b7c1c-142">Neu – AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b7c1c-142">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="b7c1c-143">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b7c1c-143">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="b7c1c-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b7c1c-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

