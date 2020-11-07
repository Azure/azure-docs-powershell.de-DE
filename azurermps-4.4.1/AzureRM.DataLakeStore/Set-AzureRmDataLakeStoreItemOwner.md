---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: fc71ec338303876a2cff44a07632e9fae5d3d2d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665387"
---
# <span data-ttu-id="5d504-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="5d504-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="5d504-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d504-102">SYNOPSIS</span></span>
<span data-ttu-id="5d504-103">Ändert den Besitzer einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5d504-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d504-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d504-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d504-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d504-105">DESCRIPTION</span></span>
<span data-ttu-id="5d504-106">Das Cmdlet " **Satz-AzureRmDataLakeStoreItemOwner** " ändert den Besitzer einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5d504-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5d504-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d504-107">EXAMPLES</span></span>

### <span data-ttu-id="5d504-108">Beispiel 1: Einrichten des Besitzers für ein Element</span><span class="sxs-lookup"><span data-stu-id="5d504-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="5d504-109">Dieser Befehl legt den Besitzer für das Stammverzeichnis auf Patti Fuller fest.</span><span class="sxs-lookup"><span data-stu-id="5d504-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="5d504-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d504-110">PARAMETERS</span></span>

### <span data-ttu-id="5d504-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="5d504-111">-Account</span></span>
<span data-ttu-id="5d504-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="5d504-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5d504-113">-ID</span><span class="sxs-lookup"><span data-stu-id="5d504-113">-Id</span></span>
<span data-ttu-id="5d504-114">Gibt die Objekt-ID des AzureActive-Verzeichnis Benutzers, der Gruppe oder des Dienst Prinzipals an, der als Besitzer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d504-114">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d504-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d504-115">-PassThru</span></span>
<span data-ttu-id="5d504-116">Gibt an, dass der resultierende aktualisierte Besitzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d504-116">Indicates the resulting updated owner should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d504-117">-Path</span><span class="sxs-lookup"><span data-stu-id="5d504-117">-Path</span></span>
<span data-ttu-id="5d504-118">Gibt den Daten See-Speicherpfad des zu ändernden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="5d504-118">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d504-119">-Typ</span><span class="sxs-lookup"><span data-stu-id="5d504-119">-Type</span></span>
<span data-ttu-id="5d504-120">Gibt den Typ des festzulegenden Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="5d504-120">Specifies the type of owner to set.</span></span>
<span data-ttu-id="5d504-121">Die zulässigen Werte für diesen Parameter sind: Benutzer und Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5d504-121">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d504-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d504-122">-Confirm</span></span>
<span data-ttu-id="5d504-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d504-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d504-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d504-124">-WhatIf</span></span>
<span data-ttu-id="5d504-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d504-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d504-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d504-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d504-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d504-127">-DefaultProfile</span></span>
<span data-ttu-id="5d504-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d504-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d504-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d504-129">CommonParameters</span></span>
<span data-ttu-id="5d504-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d504-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d504-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d504-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d504-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d504-132">INPUTS</span></span>

## <span data-ttu-id="5d504-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d504-133">OUTPUTS</span></span>

### <span data-ttu-id="5d504-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5d504-134">string</span></span>
<span data-ttu-id="5d504-135">Wenn passthru angegeben ist, wird der aktualisierte Besitzer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5d504-135">If PassThru is specified, returns the updated owner.</span></span>

## <span data-ttu-id="5d504-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d504-136">NOTES</span></span>

## <span data-ttu-id="5d504-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d504-137">RELATED LINKS</span></span>

[<span data-ttu-id="5d504-138">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="5d504-138">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)


