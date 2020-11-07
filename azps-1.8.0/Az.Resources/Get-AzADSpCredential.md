---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 5307e070f8c568473e1ce35f1183517cd3def05c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659655"
---
# <span data-ttu-id="ae4f5-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ae4f5-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="ae4f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae4f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4f5-103">Ruft eine Liste mit Anmeldeinformationen ab, die einem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ae4f5-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="ae4f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae4f5-104">SYNTAX</span></span>

### <span data-ttu-id="ae4f5-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ae4f5-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae4f5-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae4f5-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae4f5-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae4f5-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae4f5-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae4f5-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae4f5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae4f5-109">DESCRIPTION</span></span>
<span data-ttu-id="ae4f5-110">Mithilfe des Get-AzADSpCredential-Cmdlets können Sie eine Liste mit Anmeldeinformationen abrufen, die einem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ae4f5-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="ae4f5-111">Dieser Befehl ruft alle Anmelde Informationseigenschaften (aber nicht den Anmelde Informationswert) ab, die dem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ae4f5-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="ae4f5-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae4f5-112">EXAMPLES</span></span>

### <span data-ttu-id="ae4f5-113">Beispiel 1 – Listen Anmeldeinformationen nach SPN</span><span class="sxs-lookup"><span data-stu-id="ae4f5-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="ae4f5-114">Gibt eine Liste der Anmeldeinformationen zurück, die dem Dienstprinzipal mit SPN ' ' zugeordnet sind http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="ae4f5-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="ae4f5-115">Beispiel 2: Auflisten von Anmeldeinformationen nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="ae4f5-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="ae4f5-116">Gibt eine Liste der Anmeldeinformationen zurück, die dem Dienstprinzipal mit der Objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ae4f5-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="ae4f5-117">Beispiel für 3-Listen-Anmeldeinformationen durch Piping</span><span class="sxs-lookup"><span data-stu-id="ae4f5-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="ae4f5-118">Ruft den Dienstprinzipal mit der Objekt-ID "58e28616-99cc-4da4-b705-7672130e1047" ab und leitet ihn an das Get-AzADSpCredential-Cmdlet weiter, um alle Anmeldeinformationen für diesen Dienstprinzipal aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="ae4f5-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="ae4f5-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae4f5-119">PARAMETERS</span></span>

### <span data-ttu-id="ae4f5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4f5-120">-DefaultProfile</span></span>
<span data-ttu-id="ae4f5-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ae4f5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae4f5-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ae4f5-122">-DisplayName</span></span>
<span data-ttu-id="ae4f5-123">Der Anzeigename des Dienst Prinzipals</span><span class="sxs-lookup"><span data-stu-id="ae4f5-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="ae4f5-124">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="ae4f5-124">-ObjectId</span></span>
<span data-ttu-id="ae4f5-125">Die Objekt-ID des Dienst Prinzipals, von dem die Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ae4f5-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae4f5-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ae4f5-126">-ServicePrincipalName</span></span>
<span data-ttu-id="ae4f5-127">Der Name (SPN) des Dienst Prinzipals, aus dem Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ae4f5-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="ae4f5-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="ae4f5-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="ae4f5-129">Das Dienstprinzipal Objekt, aus dem die Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ae4f5-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae4f5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4f5-130">CommonParameters</span></span>
<span data-ttu-id="ae4f5-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae4f5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4f5-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae4f5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4f5-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae4f5-133">INPUTS</span></span>

### <span data-ttu-id="ae4f5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ae4f5-134">System.String</span></span>

### <span data-ttu-id="ae4f5-135">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ae4f5-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="ae4f5-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae4f5-136">OUTPUTS</span></span>

### <span data-ttu-id="ae4f5-137">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="ae4f5-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="ae4f5-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae4f5-138">NOTES</span></span>

## <span data-ttu-id="ae4f5-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae4f5-139">RELATED LINKS</span></span>

[<span data-ttu-id="ae4f5-140">Neu – AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ae4f5-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="ae4f5-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ae4f5-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="ae4f5-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ae4f5-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

