---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 7c60e6cfca0cc045d016dd763f0b64b0ad3c6550
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483013"
---
# <span data-ttu-id="c24c3-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="c24c3-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="c24c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c24c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c24c3-103">Ändert ein Kennwort für die Anmeldeinformationen des Azure Data Lake Analytics-Katalogs.</span><span class="sxs-lookup"><span data-stu-id="c24c3-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c24c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c24c3-104">SYNTAX</span></span>

### <span data-ttu-id="c24c3-105">SetByHostNameAndPort (Standard)</span><span class="sxs-lookup"><span data-stu-id="c24c3-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c24c3-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="c24c3-106">SetByFullURI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c24c3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c24c3-107">DESCRIPTION</span></span>
<span data-ttu-id="c24c3-108">Mit dem Set-AzureRmDataLakeAnalyticsCatalogCredential-Cmdlet wird ein Anmelde Informations Kennwort geändert, das einem Azure Data Lake-Analyse Katalog zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c24c3-108">The Set-AzureRmDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="c24c3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c24c3-109">EXAMPLES</span></span>

### <span data-ttu-id="c24c3-110">Beispiel 1: Ändern des Kennworts für ein Anmelde Informations Konto</span><span class="sxs-lookup"><span data-stu-id="c24c3-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="c24c3-111">Mit diesem Befehl wird das Kennwort für die Anmeldeinformationen auf das in "neues Kennwort" angegebene Kennwort festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c24c3-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="c24c3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c24c3-112">PARAMETERS</span></span>

### <span data-ttu-id="c24c3-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="c24c3-113">-Account</span></span>
<span data-ttu-id="c24c3-114">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="c24c3-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24c3-115">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="c24c3-115">-Credential</span></span>
<span data-ttu-id="c24c3-116">Gibt den Namen und das aktuelle Kennwort der zu ändernden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="c24c3-116">Specifies the name and current password of the credential to modify.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24c3-117">-Credentialname</span><span class="sxs-lookup"><span data-stu-id="c24c3-117">-CredentialName</span></span>
<span data-ttu-id="c24c3-118">Gibt den Namen der zu ändernden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="c24c3-118">Specifies the name of the credential to modify</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24c3-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="c24c3-119">-DatabaseHost</span></span>
<span data-ttu-id="c24c3-120">Gibt den Hostnamen der externen Datenquelle an, mit der die Anmeldeinformationen im Format MyDatabase.contoso.com eine Verbindung herstellen können.</span><span class="sxs-lookup"><span data-stu-id="c24c3-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: SetByFullURI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24c3-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c24c3-121">-DatabaseName</span></span>
<span data-ttu-id="c24c3-122">Gibt den Namen der Datenbank im Data Lake Analytics-Konto an, in dem die Anmeldeinformationen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c24c3-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24c3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24c3-123">-DefaultProfile</span></span>
<span data-ttu-id="c24c3-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c24c3-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24c3-125">-Neues Kennwort</span><span class="sxs-lookup"><span data-stu-id="c24c3-125">-NewPassword</span></span>
<span data-ttu-id="c24c3-126">Gibt das neue Kennwort für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="c24c3-126">Specifies the new password for the credential</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24c3-127">-Port</span><span class="sxs-lookup"><span data-stu-id="c24c3-127">-Port</span></span>
<span data-ttu-id="c24c3-128">Gibt die Portnummer an, die zum Herstellen einer Verbindung mit dem angegebenen DatabaseHost mithilfe dieser Anmeldeinformationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c24c3-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByFullURI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24c3-129">-URI</span><span class="sxs-lookup"><span data-stu-id="c24c3-129">-Uri</span></span>
<span data-ttu-id="c24c3-130">Gibt den vollständigen Uniform Resource Identifier (URI) der externen Datenquelle an, mit der diese Anmeldeinformationen eine Verbindung herstellen können.</span><span class="sxs-lookup"><span data-stu-id="c24c3-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: Uri
Parameter Sets: SetByHostNameAndPort
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c24c3-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c24c3-131">-Confirm</span></span>
<span data-ttu-id="c24c3-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c24c3-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24c3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c24c3-133">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24c3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24c3-134">CommonParameters</span></span>
<span data-ttu-id="c24c3-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c24c3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24c3-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c24c3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24c3-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c24c3-137">INPUTS</span></span>

### <span data-ttu-id="c24c3-138">Keine</span><span class="sxs-lookup"><span data-stu-id="c24c3-138">None</span></span>
<span data-ttu-id="c24c3-139">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c24c3-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c24c3-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c24c3-140">OUTPUTS</span></span>

### <span data-ttu-id="c24c3-141">Keine</span><span class="sxs-lookup"><span data-stu-id="c24c3-141">None</span></span>

## <span data-ttu-id="c24c3-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="c24c3-142">NOTES</span></span>

## <span data-ttu-id="c24c3-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c24c3-143">RELATED LINKS</span></span>

