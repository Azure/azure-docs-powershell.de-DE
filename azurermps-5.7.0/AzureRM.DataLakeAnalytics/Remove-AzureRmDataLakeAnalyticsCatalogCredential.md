---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: af6acce52ee41297e650abb76188324ecf313679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481262"
---
# <span data-ttu-id="92724-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="92724-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="92724-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92724-102">SYNOPSIS</span></span>
<span data-ttu-id="92724-103">Löscht eine Azure Data Lake-Analyse Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="92724-103">Deletes an Azure Data Lake Analytics credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92724-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92724-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92724-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92724-105">DESCRIPTION</span></span>
<span data-ttu-id="92724-106">Das Remove-AzureRmDataLakeAnalyticsCatalogCredential-Cmdlet löscht eine Azure Data Lake Analytics-Katalog Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="92724-106">The Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="92724-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92724-107">EXAMPLES</span></span>

### <span data-ttu-id="92724-108">Beispiel 1: Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="92724-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="92724-109">Mit diesem Befehl werden die Anmeldeinformationen für den angegebenen Data Lake Analytics-Katalog entfernt.</span><span class="sxs-lookup"><span data-stu-id="92724-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="92724-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="92724-110">PARAMETERS</span></span>

### <span data-ttu-id="92724-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="92724-111">-Account</span></span>
<span data-ttu-id="92724-112">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="92724-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="92724-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="92724-113">-DatabaseName</span></span>
<span data-ttu-id="92724-114">Gibt den Namen der Datenbank an, die die Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="92724-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="92724-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92724-115">-DefaultProfile</span></span>
<span data-ttu-id="92724-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="92724-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92724-117">-Force</span><span class="sxs-lookup"><span data-stu-id="92724-117">-Force</span></span>
<span data-ttu-id="92724-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="92724-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92724-119">-Name</span><span class="sxs-lookup"><span data-stu-id="92724-119">-Name</span></span>
<span data-ttu-id="92724-120">Gibt den Namen der Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="92724-120">Specifies the name of the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92724-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92724-121">-PassThru</span></span>
<span data-ttu-id="92724-122">Gibt an, dass dieses Cmdlet nicht wartet, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="92724-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="92724-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="92724-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="92724-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="92724-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92724-125">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="92724-125">-Password</span></span>
<span data-ttu-id="92724-126">Das Kennwort für die Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="92724-126">The password for the credential.</span></span>
<span data-ttu-id="92724-127">Dies ist erforderlich, wenn der Anrufer nicht der Besitzer des Kontos ist.</span><span class="sxs-lookup"><span data-stu-id="92724-127">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92724-128">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="92724-128">-Recurse</span></span>
<span data-ttu-id="92724-129">Gibt an, dass dieser Löschvorgang durchlaufen und auch alle Ressourcen, die von diesen Anmeldeinformationen abhängig sind, gelöscht und gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="92724-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92724-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92724-130">-Confirm</span></span>
<span data-ttu-id="92724-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92724-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92724-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92724-132">-WhatIf</span></span>
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

### <span data-ttu-id="92724-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92724-133">CommonParameters</span></span>
<span data-ttu-id="92724-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92724-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92724-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92724-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92724-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92724-136">INPUTS</span></span>

### <span data-ttu-id="92724-137">Keine</span><span class="sxs-lookup"><span data-stu-id="92724-137">None</span></span>
<span data-ttu-id="92724-138">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="92724-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="92724-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92724-139">OUTPUTS</span></span>

### <span data-ttu-id="92724-140">bool</span><span class="sxs-lookup"><span data-stu-id="92724-140">bool</span></span>
<span data-ttu-id="92724-141">Wenn passthru angegeben ist, gibt true nach Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="92724-141">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="92724-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="92724-142">NOTES</span></span>

## <span data-ttu-id="92724-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92724-143">RELATED LINKS</span></span>

