---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 4f7a391228529cdb28951b6b3f3f792e8d0de395
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170856"
---
# <span data-ttu-id="27e64-101">New-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="27e64-101">New-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="27e64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27e64-102">SYNOPSIS</span></span>
<span data-ttu-id="27e64-103">Erstellt einen neuen Azure Data Lake Analytics-Katalog als Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="27e64-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="27e64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27e64-104">SYNTAX</span></span>

### <span data-ttu-id="27e64-105">CreateByHostNameAndPort (Standard)</span><span class="sxs-lookup"><span data-stu-id="27e64-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27e64-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="27e64-106">CreateByFullURI</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27e64-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27e64-107">DESCRIPTION</span></span>
<span data-ttu-id="27e64-108">Das New-AzDataLakeAnalyticsCatalogCredential cmdlet erstellt neue Anmeldeinformationen zur Verwendung in einem Azure Data Lake Analytics-Katalog zum Herstellen einer Verbindung mit externen Datenquellen.</span><span class="sxs-lookup"><span data-stu-id="27e64-108">The New-AzDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="27e64-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27e64-109">EXAMPLES</span></span>

### <span data-ttu-id="27e64-110">Beispiel 1: Erstellen von Anmeldeinformationen für einen Katalog mit Angabe von Host und Port</span><span class="sxs-lookup"><span data-stu-id="27e64-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="27e64-111">Mit diesem Befehl werden die angegebenen Anmeldeinformationen für das angegebene Konto, die Datenbank, den Host und den Port mithilfe des https-Protokolls erstellt.</span><span class="sxs-lookup"><span data-stu-id="27e64-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="27e64-112">Beispiel 2: Erstellen von Anmeldeinformationen für einen Katalog mit vollständiger URI</span><span class="sxs-lookup"><span data-stu-id="27e64-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="27e64-113">Mit diesem Befehl werden die angegebenen Anmeldeinformationen für den angegebenen Konto-, Datenbank- und externen Datenquellen-URI erstellt.</span><span class="sxs-lookup"><span data-stu-id="27e64-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="27e64-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27e64-114">PARAMETERS</span></span>

### <span data-ttu-id="27e64-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="27e64-115">-Account</span></span>
<span data-ttu-id="27e64-116">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="27e64-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e64-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="27e64-117">-Credential</span></span>
<span data-ttu-id="27e64-118">Gibt den Benutzernamen und das entsprechende Kennwort der Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="27e64-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e64-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="27e64-119">-CredentialName</span></span>
<span data-ttu-id="27e64-120">Gibt den Namen und das Kennwort der Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="27e64-120">Specifies the name and password of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e64-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="27e64-121">-DatabaseHost</span></span>
<span data-ttu-id="27e64-122">Gibt den Hostnamen der externen Datenquelle an, zu der die Anmeldeinformationen im Format mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="27e64-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e64-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="27e64-123">-DatabaseName</span></span>
<span data-ttu-id="27e64-124">Gibt den Namen der Datenbank im Data Lake Analytics-Konto an, in der die Anmeldeinformationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="27e64-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e64-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e64-125">-DefaultProfile</span></span>
<span data-ttu-id="27e64-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="27e64-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27e64-127">-Port</span><span class="sxs-lookup"><span data-stu-id="27e64-127">-Port</span></span>
<span data-ttu-id="27e64-128">Gibt die Portnummer an, die verwendet wird, um mit diesen Anmeldeinformationen eine Verbindung mit dem angegebenen DatabaseHost herzustellen.</span><span class="sxs-lookup"><span data-stu-id="27e64-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e64-129">-URI</span><span class="sxs-lookup"><span data-stu-id="27e64-129">-Uri</span></span>
<span data-ttu-id="27e64-130">Gibt den vollständigen URI (Uniform Resource Identifier) der externen Datenquelle an, mit der diese Anmeldeinformationen eine Verbindung herstellen können.</span><span class="sxs-lookup"><span data-stu-id="27e64-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e64-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27e64-131">-Confirm</span></span>
<span data-ttu-id="27e64-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27e64-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e64-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="27e64-133">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e64-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e64-134">CommonParameters</span></span>
<span data-ttu-id="27e64-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27e64-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e64-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27e64-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e64-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27e64-137">INPUTS</span></span>

### <span data-ttu-id="27e64-138">System.String</span><span class="sxs-lookup"><span data-stu-id="27e64-138">System.String</span></span>

### <span data-ttu-id="27e64-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="27e64-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="27e64-140">System.URI</span><span class="sxs-lookup"><span data-stu-id="27e64-140">System.Uri</span></span>

### <span data-ttu-id="27e64-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="27e64-141">System.Int32</span></span>

## <span data-ttu-id="27e64-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27e64-142">OUTPUTS</span></span>

### <span data-ttu-id="27e64-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="27e64-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="27e64-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="27e64-144">NOTES</span></span>

## <span data-ttu-id="27e64-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="27e64-145">RELATED LINKS</span></span>
