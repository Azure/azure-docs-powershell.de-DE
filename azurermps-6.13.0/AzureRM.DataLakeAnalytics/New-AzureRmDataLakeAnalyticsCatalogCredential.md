---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 2d239e8c40c4e2472ee26a2f08b14a8f7871bd80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502126"
---
# <span data-ttu-id="4e7ba-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="4e7ba-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="4e7ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e7ba-102">SYNOPSIS</span></span>
<span data-ttu-id="4e7ba-103">Erstellt eine neue Anmeldeinformationen für Azure Data Lake Analytics-Katalog.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e7ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e7ba-104">SYNTAX</span></span>

### <span data-ttu-id="4e7ba-105">CreateByHostNameAndPort (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e7ba-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e7ba-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="4e7ba-106">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e7ba-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e7ba-107">DESCRIPTION</span></span>
<span data-ttu-id="4e7ba-108">Das New-AzureRmDataLakeAnalyticsCatalogCredential-Cmdlet erstellt eine neue Anmeldeinformationen, die in einem Azure Data Lake-Analyse Katalog zum Herstellen einer Verbindung mit externen Datenquellen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-108">The New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="4e7ba-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e7ba-109">EXAMPLES</span></span>

### <span data-ttu-id="4e7ba-110">Beispiel 1: Erstellen einer Anmeldeinformationen für einen Katalog, der Host und Port angibt</span><span class="sxs-lookup"><span data-stu-id="4e7ba-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="4e7ba-111">Mit diesem Befehl werden die angegebenen Anmeldeinformationen für das angegebene Konto, die Datenbank, den Host und den Port mithilfe des HTTPS-Protokolls erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="4e7ba-112">Beispiel 2: Erstellen einer Anmeldeinformationen für einen Katalog mit Angabe des vollständigen URIs</span><span class="sxs-lookup"><span data-stu-id="4e7ba-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="4e7ba-113">Mit diesem Befehl werden die angegebenen Anmeldeinformationen für das angegebene Konto, die Datenbank und den externen Datenquellen-URI erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="4e7ba-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e7ba-114">PARAMETERS</span></span>

### <span data-ttu-id="4e7ba-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="4e7ba-115">-Account</span></span>
<span data-ttu-id="4e7ba-116">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4e7ba-117">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="4e7ba-117">-Credential</span></span>
<span data-ttu-id="4e7ba-118">Gibt den Benutzernamen und das entsprechende Kennwort für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-118">Specifies the user name and corresponding password of the credential.</span></span>

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

### <span data-ttu-id="4e7ba-119">-Credentialname</span><span class="sxs-lookup"><span data-stu-id="4e7ba-119">-CredentialName</span></span>
<span data-ttu-id="4e7ba-120">Gibt den Namen und das Kennwort für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="4e7ba-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="4e7ba-121">-DatabaseHost</span></span>
<span data-ttu-id="4e7ba-122">Gibt den Hostnamen der externen Datenquelle an, mit der die Anmeldeinformationen im Format MyDatabase.contoso.com eine Verbindung herstellen können.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="4e7ba-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e7ba-123">-DatabaseName</span></span>
<span data-ttu-id="4e7ba-124">Gibt den Namen der Datenbank im Data Lake Analytics-Konto an, in dem die Anmeldeinformationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

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

### <span data-ttu-id="4e7ba-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e7ba-125">-DefaultProfile</span></span>
<span data-ttu-id="4e7ba-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4e7ba-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e7ba-127">-Port</span><span class="sxs-lookup"><span data-stu-id="4e7ba-127">-Port</span></span>
<span data-ttu-id="4e7ba-128">Gibt die Portnummer an, die zum Herstellen einer Verbindung mit dem angegebenen DatabaseHost mithilfe dieser Anmeldeinformationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="4e7ba-129">-URI</span><span class="sxs-lookup"><span data-stu-id="4e7ba-129">-Uri</span></span>
<span data-ttu-id="4e7ba-130">Gibt den vollständigen Uniform Resource Identifier (URI) der externen Datenquelle an, mit der diese Anmeldeinformationen eine Verbindung herstellen können.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="4e7ba-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4e7ba-131">-Confirm</span></span>
<span data-ttu-id="4e7ba-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e7ba-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e7ba-133">-WhatIf</span></span>
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

### <span data-ttu-id="4e7ba-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e7ba-134">CommonParameters</span></span>
<span data-ttu-id="4e7ba-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e7ba-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e7ba-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e7ba-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e7ba-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e7ba-137">INPUTS</span></span>

### <span data-ttu-id="4e7ba-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4e7ba-138">System.String</span></span>

### <span data-ttu-id="4e7ba-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="4e7ba-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="4e7ba-140">System. Uri</span><span class="sxs-lookup"><span data-stu-id="4e7ba-140">System.Uri</span></span>

### <span data-ttu-id="4e7ba-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4e7ba-141">System.Int32</span></span>

## <span data-ttu-id="4e7ba-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e7ba-142">OUTPUTS</span></span>

### <span data-ttu-id="4e7ba-143">Microsoft. Azure. Management. datalake. Analytics. Models. USqlCredential</span><span class="sxs-lookup"><span data-stu-id="4e7ba-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="4e7ba-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e7ba-144">NOTES</span></span>

## <span data-ttu-id="4e7ba-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e7ba-145">RELATED LINKS</span></span>
